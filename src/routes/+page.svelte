<svelte:head>
	<title>L'esthétique AA - Esthéticienne à domicile à Oullins et alentours</title>
	<meta name="description" content="..." />
	<meta name="keywords" content="..." />
	<meta name="google-site-verification" content="K9H81I_EzYQIRoguOVlhwiUmBY0jgxy2GawD07KDM8A" />

	
    <script>
        function getCookie(name) {
            const value = `; ${document.cookie}`;
            const parts = value.split(`; ${name}=`);
            if (parts.length === 2) return parts.pop().split(";").shift();
        }

        function loadFbPixel() {
            if (window.fbq) return;

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
                t.src = "https://connect.facebook.net/en_US/fbevents.js";
                s = b.getElementsByTagName(e)[0];
                s.parentNode.insertBefore(t, s);
            })(window, document, "script");

            fbq("init", "669075309377526");
            fbq("track", "PageView");
			fbq('track', 'ViewContent');
			fbq("track", "Contact");
        }


        $: {

            if (typeof window !== 'undefined') {
                setTimeout(() => {
					console.log(window.tarteaucitron?.state?.facebookpixel);
                    if (window.tarteaucitron?.state?.facebookpixel === true) {
                        loadFbPixel();
                    }
                }, 500);
            }
        }
    </script>
</svelte:head>

<script>
	import Instagram from '$lib/images/Instagram.webp';
	import Facebook from '$lib/images/Facebook.png';
	import Prestations from '$lib/prestations.svelte';
	import About from '$lib/about.svelte';
	import Payment from '$lib/payment.svelte';
	import FAQ from '$lib/faq.svelte';
	import Reviews from '$lib/review.svelte';
	import { page } from '$app/stores';
	import Brochure from '$lib/images/Beige Organic Beauty and Spa Brochure.pdf';
</script>

<div class="page-home">
	<div class="home-page-container">
		<div class="page-container">
			<div class="container">
				<div class="content">
					<h1>L'esthétiqueAA</h1>

					<p class="tagline">La beauté au naturel, dans le confort de votre maison</p>

					<p class="description">
					<i>
						"Profitez de soins esthétiques 100% féminins à domicile : <br />
						<b>Massages bien-être, épilations douces, soins des ongles</b><br />
						Dans une atmosphère de bienveillance et de douceur." </i>
					</p>

					<div class="button">
						<button class="construction-btn" on:click={() => window.location.href = '#prestations'}>
							<b>Découvrir les prestations ✨</b>
						</button>
						<button class="construction-btn" on:click={() => window.location.href = '/contact'}>
							<b>Prendre rendez-vous 💄</b>
						</button>
					</div>

					<p class="follow-us-localisation">
						📍 On se déplace sur : Oullins, Saint-Genis-Laval, Sainte-Foy-lès-Lyon, La Mulatière, Tassin, Millery, Charly, Vernaison, Irigny, Brignais, Chaponost, Pierre-Bénite
					</p>
					<p class="follow-us-localisation">Déplacements possibles dans les communes voisines, n'hésitez pas à nous contacter pour en savoir plus.</p>

					<div class="social-icons">
						<a href="https://www.facebook.com/share/HbRySNxzmWmYTA8G/" target="_blank"><img src={Facebook} alt="Facebook" /></a>
						<a href="https://www.instagram.com/anaisdelice.estheticienne69" target="_blank"><img src={Instagram} alt="Instagram" /></a>
					</div>
					<p class="follow-us">📲 Retrouvez-nous sur les réseaux sociaux</p>
				</div>
			</div>
		</div>
	</div>
	<Prestations />
	<About />
	<Payment />
	<Reviews/>
	<FAQ />
</div>