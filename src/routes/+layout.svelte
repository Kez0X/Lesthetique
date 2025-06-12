<svelte:head>
  <script src="https://cdn.jsdelivr.net/npm/tarteaucitronjs@latest/tarteaucitron.min.js"></script>
  <script>
    let tarteauReady = false;

    function openPanel() {
      const sel = '#tarteaucitronManager';
      const el = document.querySelector(sel);
      if (el) {
        el.click();
        console.log('[Tarteaucitron] Panneau ouvert via', sel);
      } else {
        console.warn('[Tarteaucitron] Sélecteur non trouvé pour ouvrir le panneau');
      }
    }

    const initTarteaucitron = () => {
      tarteaucitron.init({
        privacyUrl: "/politique_de_confidentialite",
        hashtag: "#tarteaucitron",
        cookieName: "tarteaucitron",
        orientation: "middle",
        showAlertSmall: false,
        showIcon: true,
        iconPosition: "BottomRight",
        DenyAllCta: true,
        AcceptAllCta: true,
        highPrivacy: true,
        handleBrowserDNTRequest: false,
        mandatory: true
      });

      tarteaucitron.job = ['ads', 'analytics'];
    };

    const interval = setInterval(() => {
      if (window.tarteaucitron && !tarteauReady) {
        tarteauReady = true;
        clearInterval(interval);

        // Déclaration des services
        tarteaucitron.services.ads = {
          key: "ads",
          type: "ads",
          name: "Publicités",
          needConsent: true,
          cookies: ["_ga"],
          js: function() {
            (function(w, d, s, l, i) {
              w[l] = w[l] || [];
              w[l].push({ 'gtm.start': new Date().getTime(), event: 'gtm.js' });
              const f = d.getElementsByTagName(s)[0];
              const j = d.createElement(s);
              const dl = l !== 'dataLayer' ? '&l=' + l : '';
              j.async = true;
              j.src = 'https://www.googletagmanager.com/gtm.js?id=' + i + dl;
              f.parentNode.insertBefore(j, f);
            })(window, document, 'script', 'dataLayer', 'GTM-PRV5CSBW');
          },
          fallback: function() {}
        };
        
        tarteaucitron.services.analytics = {
          key: "analytics",
          type: "analytics",
          name: "Statistiques",
          needConsent: true,
          cookies: [],
          js: function() {},
          fallback: function() {}
        };

        // Initialisation initiale
        initTarteaucitron();

        // Surveillance du cookie
        let previous = tarteaucitron.cookie.read('tarteaucitron');
        setInterval(() => {
          const current = tarteaucitron.cookie.read('tarteaucitron');
          if (previous && !current) {
            console.log('[Tarteaucitron] Cookie supprimé, réouverture du panneau');
            openPanel();
          }
          previous = current;
        }, 5000);
      }
    }, 100);
  </script>
</svelte:head>

<script>
  import Navbar from '$lib/navbar.svelte';
  import Footer from '$lib/footer.svelte';
  import { injectAnalytics } from '@vercel/analytics/sveltekit';
  import '../app.css';

  injectAnalytics();
</script>

<div class="app">
  <Navbar />
  <slot />
  <Footer />
</div>
