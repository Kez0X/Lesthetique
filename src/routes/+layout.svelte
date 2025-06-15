<svelte:head>
<!-- <script src="https://cdn.jsdelivr.net/npm/tarteaucitronjs@latest/tarteaucitron.min.js"></script>
<script>
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

  // Configuration de tarteaucitron
  const tacConfig = {
    privacyUrl: "/politique_de_confidentialite",
    hashtag: "#tarteaucitron",
    cookieName: "tarteaucitron",
    orientation: "middle",
    showAlertSmall: true,
    showIcon: true,
    AdBlocker: false,
    AcceptAllCta: true,
    DenyAllCta: true,
    iconPosition: "BottomLeft",
    highPrivacy: true,
    removeCredit: true,
    moreInfoLink: true,
    groupServices: true,
    showDetailsOnClick: true,
    serviceDefaultState: "wait",
    readmoreLink: "/politique-de-cookies"
  };

  // Fonction pour envoyer l'événement cookie_choose à GTM
  const sendCookieChoiceEvent = (choice) => {
    if (window.dataLayer) {
      window.dataLayer.push({
        event: 'cookie_choose',
        cookie_choice: choice
      });
      console.log('[GTM] Event cookie_choose envoyé avec le choix:', choice);
    } else {
      console.error('[GTM] dataLayer non disponible');
    }
  };

  // Détection du choix de l'utilisateur
  const monitorCookieChoice = () => {
    // Écoute les changements sur le cookie tarteaucitron
    let lastCookieValue = tarteaucitron.cookie.read();

    const checkCookieChange = () => {
      const currentCookieValue = tarteaucitron.cookie.read();
      
      if (currentCookieValue !== lastCookieValue) {
        console.log('[TAC] Changement de cookie détecté:', currentCookieValue);
        lastCookieValue = currentCookieValue;
        
        // Envoyer l'événement seulement si c'est un nouveau choix (pas la première lecture)
        if (currentCookieValue) {
          sendCookieChoiceEvent(currentCookieValue);
        }
      }
    };

    // Vérifier périodiquement les changements
    setInterval(checkCookieChange, 1000);

    // Écouter les événements de tarteaucitron
    if (typeof tarteaucitron.userInterface !== 'undefined') {
      tarteaucitron.userInterface.responder = function (type, service) {
        if (type === 'allow' || type === 'deny' || type === 'acceptAll' || type === 'denyAll') {
          setTimeout(() => {
            const choice = tarteaucitron.cookie.read();
            sendCookieChoiceEvent(choice);
          }, 500); // Petit délai pour s'assurer que le cookie est bien mis à jour
        }
      };
    }
  };

  // Initialisation robuste de tarteaucitron
  const initTAC = () => {
    try {
      tarteaucitron.init(tacConfig);
      tarteaucitron.job = ['ads', 'analytics'];
      console.log('[TAC] Initialisation réussie');
      
      // Démarrer la surveillance des choix de cookies
      monitorCookieChoice();
      
      return true;
    } catch (e) {
      console.error('[TAC] Erreur lors de l\'initialisation:', e);
      return false;
    }
  };

  // Fonction pour ouvrir le panel COMPLET de manière robuste
  const openFullPanelSafely = () => {
    const maxAttempts = 10;
    const interval = 300;
    let attempts = 0;

    const tryOpen = () => {
      attempts++;
      
      if (typeof tarteaucitron.userInterface === 'undefined') {
        if (attempts < maxAttempts) {
          setTimeout(tryOpen, interval);
        }
        return;
      }

      try {
        tarteaucitron.userInterface.openPanel();
        console.log('[TAC] Panel complet ouvert avec succès');
      } catch (e) {
        console.error('[TAC] Erreur lors de l\'ouverture du panel complet:', e);
      }
    };

    tryOpen();
  };

  // Vérifie l'état des cookies et ouvre le panel COMPLET si nécessaire
  const checkConsent = () => {
    try {
      const hasConsent = tarteaucitron.cookie.read('tarteaucitron');
      const panel = document.getElementById('tarteaucitron');
      const panelVisible = panel && panel.style.display === 'block';

      if (!hasConsent && !panelVisible) {
        console.log('[TAC] Aucun consentement trouvé, ouverture du panel complet');
        if (initTAC()) {
          openFullPanelSafely();
        }
      }
    } catch (e) {
      console.error('[TAC] Erreur lors de la vérification du consentement:', e);
    }
  };

  // Surveille les changements de cookies
  const setupCookieMonitoring = () => {
    // Vérification périodique
    setInterval(checkConsent, 5000);

    // Détection des changements dans le stockage
    const originalSetItem = localStorage.setItem;
    localStorage.setItem = function(key, value) {
      originalSetItem.apply(this, arguments);
      if (key === 'tarteaucitron') {
        setTimeout(checkConsent, 1000);
      }
    };

    // Détection des suppressions de cookies
    document.cookie = 'tarteaucitron=; expires=Thu, 01 Jan 1970 00:00:00 GMT';
    const originalRemoveItem = localStorage.removeItem;
    localStorage.removeItem = function(key) {
      originalRemoveItem.apply(this, arguments);
      if (key === 'tarteaucitron') {
        setTimeout(checkConsent, 1000);
      }
    };
  };

  // Initialisation principale
  const initializeTAC = () => {
    if (window.tarteaucitron) {
      if (initTAC()) {
        setupCookieMonitoring();
      }
    } else {
      console.error('[TAC] tarteaucitron.js n\'a pas été chargé correctement');
    }
  };

  // Démarrer l'initialisation lorsque la page est prête
  if ((document.readyState === 'complete' || document.readyState === 'interactive')) {
    setTimeout(initializeTAC, 0);
  } else {
    document.addEventListener('DOMContentLoaded', initializeTAC);
    window.addEventListener('load', initializeTAC);
  }
</script> -->
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
