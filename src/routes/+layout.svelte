<svelte:head>
	<script src="https://cdn.jsdelivr.net/npm/tarteaucitronjs@latest/tarteaucitron.min.js" defer></script>
	<script>
		window.addEventListener("DOMContentLoaded", () => {
			const interval = setInterval(() => {
				if (typeof tarteaucitron !== "undefined") {
					clearInterval(interval);

					tarteaucitron.init({
						privacyUrl: "/politique-de-confidentialite",
						bodyPosition: "top",
						hashtag: "#tarteaucitron",
						cookieName: "tarteaucitron",
						orientation: "middle",
						groupServices: true,
						showDetailsOnClick: true,
						serviceDefaultState: "wait",
						showAlertSmall: false,
						closePopup: true,
						showIcon: true,
						iconPosition: "BottomRight",
						DenyAllCta: true,
						AcceptAllCta: true,
						highPrivacy: true,
						mandatory: true,
						googleConsentMode: true,
						bingConsentMode: true,
						partnersList: true
					});

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

					tarteaucitron.job = tarteaucitron.job || [];
					tarteaucitron.job.push("facebookpixel");
				}
			}, 100);
		});
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
