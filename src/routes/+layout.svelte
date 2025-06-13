<svelte:head>
  <script src="https://cdn.jsdelivr.net/npm/tarteaucitronjs@latest/tarteaucitron.min.js"></script>
  <script>
    let ready = false;

    // Initialisation Tarteaucitron
    const initTAC = () => {
      tarteaucitron.init({
        privacyUrl: "/politique_de_confidentialite",
        hashtag: "#tarteaucitron",
        cookieName: "tarteaucitron",
        orientation: "middle",
        showAlertSmall: false,
        showIcon: true,
        AdBlocker: false,
        AcceptAllCta: true,
        DenyAllCta: true,
        iconPosition: "BottomRight",
        highPrivacy: true,
        removeCredit: true,
        moreInfoLink: true,
        groupServices: true,
        showDetailsOnClick: true,
        serviceDefaultState: "wait",
      });

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

      tarteaucitron.job = ['ads','analytics'];
    };

    // Ouvre le panneau complet via la méthode officielle
    const openPanel = () => {
      if (tarteaucitron.userInterface?.openPanel) {
        tarteaucitron.userInterface.openPanel();
        console.log('[TAC] Panneau complet ouvert');
      } else {
        console.warn('[TAC] openPanel non dispo, retry dans 100 ms');
        setTimeout(openPanel, 100);
      }
    };

    // Détecte la suppression du cookie ou du consentement
    const checkAndReopen = () => {
      const cookie = tarteaucitron.cookie.read('tarteaucitron');
      const panelVisible = document.getElementById('tarteaucitron')?.style.display === 'block';
      if (!cookie && !panelVisible) {
        console.log('[TAC] Consentement supprimé, réinitialisation et panneau');
        window.location.reload();
        initTAC();
      }
    };

    // Écoute les événements liés à la suppression de consentement
    const setupDetection = () => {
      ['ads_disallowed','analytics_disallowed'].forEach(evt => {
        document.addEventListener(evt, () => setTimeout(checkAndReopen, 100));
      });
      window.addEventListener('tac.close_panel', () => setTimeout(checkAndReopen, 100));
    };

    // Boucle principale : initialisation dès disponibilité de Tarteaucitron
    const mainInterval = setInterval(() => {
      if (window.tarteaucitron && !ready) {
        ready = true;
        clearInterval(mainInterval);

        initTAC();
        setupDetection();

        setInterval(checkAndReopen, 10000);
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
