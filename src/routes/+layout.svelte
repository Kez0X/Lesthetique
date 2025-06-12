<svelte:head>
  <script src="https://cdn.jsdelivr.net/npm/tarteaucitronjs@latest/tarteaucitron.min.js"></script>
  <script>
    let tarteauReady = false;

    const interval = setInterval(() => {
      if (window.tarteaucitron && !tarteauReady) {
        tarteauReady = true;
        clearInterval(interval);

        // Services déclarés une seule fois
        tarteaucitron.services.ads = {
          key: "ads",
          type: "ads",
          name: "Publicités",
          needConsent: true,
          cookies: ["_ga"],
          js: function () {
            (function(w, d, s, l, i) {
              w[l] = w[l] || [];
              w[l].push({ 'gtm.start': new Date().getTime(), event: 'gtm.js' });
              var f = d.getElementsByTagName(s)[0],
                  j = d.createElement(s),
                  dl = l != 'dataLayer' ? '&l=' + l : '';
              j.async = true;
              j.src = 'https://www.googletagmanager.com/gtm.js?id=' + i + dl;
              f.parentNode.insertBefore(j, f);
            })(window, document, 'script', 'dataLayer', 'GTM-PRV5CSBW');
          },
          fallback: function () {}
        };

        tarteaucitron.services.analytics = {
          key: "analytics",
          type: "analytics",
          name: "Statistiques",
          needConsent: true,
          cookies: [],
          js: function () {
            // volontairement vide
          },
          fallback: function () {}
        };

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

          tarteaucitron.job = tarteaucitron.job || [];
          tarteaucitron.job.push("ads");
          tarteaucitron.job.push("analytics");
        };

        // Initialisation au premier chargement
        initTarteaucitron();

        const openTarteaucitronPanel = () => {
          const icon = document.querySelector('#tarteaucitronBack');
          if (icon) {
            icon.click();
          } else {
            console.warn('Icône Tarteaucitron non trouvée');
          }
        };

        let previousCookie = tarteaucitron.cookie.read('tarteaucitron');

        setInterval(() => {
          const currentCookie = tarteaucitron.cookie.read('tarteaucitron');

          if (previousCookie && !currentCookie) {
            console.warn('[Tarteaucitron] Cookie supprimé, réouverture du panneau...');
            openTarteaucitronPanel();
          }

          previousCookie = currentCookie;
        }, 5000);
      }
    }, 100);
  </script>
</svelte:head>

<script>
  import '../app.css';
  import Navbar from '$lib/navbar.svelte';
  import Footer from '$lib/footer.svelte';
  import { injectAnalytics } from '@vercel/analytics/sveltekit';

  injectAnalytics();
</script>

<div class="app">
  <Navbar />
  <slot />
  <Footer />
</div>
