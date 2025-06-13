<svelte:head>
	<title>L'esthétique AA - Esthéticienne à domicile à Oullins et alentours</title>
	<meta name="description" content="..." />
	<meta name="keywords" content="..." />
	<meta name="google-site-verification" content="K9H81I_EzYQIRoguOVlhwiUmBY0jgxy2GawD07KDM8A" />

	<!-- Google Tag Manager -->
	<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start': new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
	j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
	'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
	})(window,document,'script','dataLayer','GTM-PRV5CSBW');</script>
	<!-- End Google Tag Manager -->

		<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-PRV5CSBW"
	height="0" width="0" title="" style="display:none;visibility:hidden"></iframe></noscript>
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
						<a class="construction-btn" href = '#prestations'>
							<b>Découvrir les prestations ✨</b>
						</a>
						<a class="construction-btn" href = '/contact'>
							<b>Prendre rendez-vous 💄</b>
						</a>
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