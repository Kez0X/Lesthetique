<svelte:head>
  <script src="https://cdn.jsdelivr.net/npm/tarteaucitronjs@latest/tarteaucitron.min.js"></script>
  <script>
    let ready = false;

    // Déclaration des services avant l'initialisation
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

    // Initialisation de Tarteaucitron
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

      // Définition des services à activer
      tarteaucitron.job = ['ads', 'analytics'];
    };

   const openPanel = () => {
      let attempts = 0;
      const maxAttempts = 50; // Limite le nombre de tentatives
      const interval = 100; // Délai entre chaque tentative en ms

      const tryOpen = () => {
        const panel = document.getElementById('tarteaucitron');
        if (panel && panel.style.display === 'block') {
          tarteaucitron.userInterface.openPanel();
          console.log('[TAC] Panneau complet ouvert');
        } else if (attempts < maxAttempts) {
          attempts++;
          console.warn(`[TAC] Tentative ${attempts}/${maxAttempts} - Panneau non disponible, nouvelle tentative dans ${interval} ms`);
          setTimeout(tryOpen, interval);
        } else {
          console.error('[TAC] Impossible d\'ouvrir le panneau, maximum de tentatives atteint');
        }
      };

      tryOpen();
    };


    // Vérification et réouverture du panneau si nécessaire
    const checkAndReopen = () => {
      const cookie = tarteaucitron.cookie.read('tarteaucitron');
      const panelVisible = document.getElementById('tarteaucitron')?.style.display === 'block';
      if (!cookie && !panelVisible) {
        console.log('[TAC] Consentement supprimé, réinitialisation et ouverture du panneau');
        initTAC();
        openPanel();
      }
    };

    // Configuration des détecteurs d'événements
    const setupDetection = () => {
      ['ads_disallowed', 'analytics_disallowed'].forEach(evt => {
        document.addEventListener(evt, () => setTimeout(checkAndReopen, 10000));
      });
      window.addEventListener('tac.close_panel', () => setTimeout(checkAndReopen, 10000));
    };

    // Intervalle principal pour l'initialisation
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
