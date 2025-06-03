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
                        !(function(f, b, e, v, n, t, s) {
                            if (f.fbq) return;
                            n = f.fbq = function () {
                                n.callMethod ? n.callMethod.apply(n, arguments) : n.queue.push(arguments);
                            };
                            if (!f._fbq) f._fbq = n;
                            n.push = n;
                            n.loaded = !0;
                            n.version = "2.0";
                            n.queue = [];
                            t = b.createElement(e);
                            t.async = !0;
                            t.src = v;
                            s = b.getElementsByTagName(e)[0];
                            s.parentNode.insertBefore(t, s);
                        })(window, document, "script", "https://connect.facebook.net/en_US/fbevents.js");

                        fbq("init", "669075309377526");
                        fbq("track", "PageView");
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
                    orientation: "bottom",
                    showAlertSmall: false,
                    showIcon: true,
                    iconPosition: "BottomRight",
                    DenyAllCta: true,
                    AcceptAllCta: true,
                    highPrivacy: false,
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
