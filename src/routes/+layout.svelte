<svelte:head>
    <script src="https://cdn.jsdelivr.net/npm/tarteaucitronjs@latest/tarteaucitron.min.js"></script>
    <script>
        let tarteauReady = false;
        const interval = setInterval(() => {
            if (window.tarteaucitron && !tarteauReady) {
                tarteauReady = true;
                clearInterval(interval);

                tarteaucitron.services.facebookpixel = {
                    key: "facebookpixel",
                    type: "ads",
                    name: "Facebook Pixel",
                    needConsent: true,
                    cookies: ["_fbp"],
                    js: function () {
                        // ne rien faire ici pour ne pas injecter le pixel automatiquement
                    },
                    fallback: function () {}
                };

                tarteaucitron.services.gtm = {
                    key: "gtm",
                    type: "api",
                    name: "Google Tag Manager",
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
                        })(window, document, 'script', 'dataLayer', 'GTM-TXSZ6PKN'); 
                    },
                    fallback: function () { return ''; }
                };

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
                tarteaucitron.job.push("facebookpixel");
                tarteaucitron.job.push("gtm");
            }
        }, 100);

    </script>
</svelte:head>
<script>
	import '../app.css';
	import Navbar from '$lib/navbar.svelte';
	import Footer from '$lib/footer.svelte';
	import { injectAnalytics } from '@vercel/analytics/sveltekit';

	// Inject Vercel Analytics lors de l'initialisation
	injectAnalytics();

</script>

<div class="app">
	<Navbar />
	<slot />
	<Footer />
</div>
