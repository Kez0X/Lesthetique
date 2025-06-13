<svelte:head>
  <script src="https://cdn.jsdelivr.net/npm/tarteaucitronjs@latest/tarteaucitron.min.js"></script>
  <script>
    let ready = false;

    // Déclaration DES SERVICES AVANT INIT !!
    tarteaucitron.services.ads = {
      key: "ads",
      type: "ads",
      name: "Publicités",
      needConsent: true,
      cookies: ["_ga"],
      js: function () {
        console.log("[TAC] Ads JS appelé");
        (function (w, d, s, l, i) {
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
      fallback: function () {}
    };

    tarteaucitron.services.analytics = {
      key: "analytics",
      type: "analytics",
      name: "Statistiques",
      needConsent: true,
      cookies: [],
      js: function () {
        console.log("[TAC] Analytics JS appelé");
      },
      fallback: function () {}
    };

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

      // Important : le job doit être défini après init()
      tarteaucitron.job = ['ads', 'analytics'];
    };

    const openPanel = () => {
      const panelReady = () => document.getElementById('tarteaucitron');

      if (!panelReady()) {
        console.warn('[TAC] Panel pas encore prêt, retry dans 100 ms');
        setTimeout(openPanel, 100);
        return;
      }

      if (tarteaucitron.userInterface?.openPanel) {
        tarteaucitron.userInterface.openPanel();
        console.log('[TAC] Panneau complet ouvert');
      } else {
        console.warn('[TAC] userInterface.openPanel non dispo, retry dans 100 ms');
        setTimeout(openPanel, 100);
      }
    };


    const checkAndReopen = () => {
      const cookie = tarteaucitron.cookie.read('tarteaucitron');
      const panelVisible = document.getElementById('tarteaucitron')?.style.display === 'block';
      if (!cookie && !panelVisible) {
        console.log('[TAC] Consentement supprimé, réinitialisation et panneau');
        initTAC();
        openPanel();
      }
    };

    const setupDetection = () => {
      ['ads_disallowed', 'analytics_disallowed'].forEach(evt => {
        document.addEventListener(evt, () => setTimeout(checkAndReopen, 10000));
      });
      window.addEventListener('tac.close_panel', () => setTimeout(checkAndReopen, 10000));
    };

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
