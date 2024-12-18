<svelte:head>
	<title>L'esthétique AA - Esthéticienne à domicile à Oullins et alentours</title>
	<meta name="description" content="Découvrez L'esthétiqueAA, spécialiste de l'esthétique à domicile pour femmes à Oullins et alentours. Prestations de massages, épilations, onglerie à domicile sur les secteurs d'Oullins, Saint-Genis-Laval, Sainte-Foy-lès-Lyon, La Mulatière, Tassin, Millery, Charly, Vernaison, Irigny, Brignais, Chaponost, Pierre-Bénite. Profitez de soins de qualité directement chez vous, dans un cadre de douceur et de professionnalisme." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthetiqueAA, l'esthetiqueAA, L'EsthetiqueAA, EsthetiqueAA, esthetiqueAA Oullins, l'esthetiqueAA Oullins, L'EsthetiqueAA Oullins, EsthetiqueAA Oullins, esthetique à domicile, esthetiqueAA domicile">
	<meta name="google-site-verification" content="K9H81I_EzYQIRoguOVlhwiUmBY0jgxy2GawD07KDM8A" />
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
					<p class="tagline">Beauté à domicile, douceur à chaque instant</p>
					<p class="description">Massages, épilations, onglerie à domicile pour femmes</p>
					<div class="button">
						<button class="construction-btn" on:click={() => window.location.href = '#prestations'}>
							<b>Nos prestations ✨</b>
						</button>
						<button class="construction-btn" on:click={() => window.location.href = '/contact'}>
							<b>Prendre rendez-vous 💄</b>
						</button>
					</div>
					<div class="button">
						<button class="construction-btn" on:click={() => window.location.href = 'https://www.planity.com/lesthetique-aa-estheticienne-a-domicile-69600-oullins-pierre-benite'}>
							<b>Prendre rendez-vous sur planity 💻</b>
						</button>
					</div>
					<p class="follow-us-localisation">Notre secteur d'activité : Oullins, Saint-Genis-Laval, Sainte-Foy-lès-Lyon, La Mulatière, Tassin
						, Millery, Charly, Vernaison, Irigny, Brignais,
						Chaponost, Pierre-bénite</p>
					<p class="follow-us" style="margin-top : 5px">Nous suivre sur les réseaux sociaux</p>
					<div class="social-icons">
						<a href="https://www.facebook.com/share/HbRySNxzmWmYTA8G/"><img src={Facebook} alt="Facebook"></a>
						<a href="https://www.instagram.com/anaisdelice.estheticienne69?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw=="><img src={Instagram} alt="Instagram"></a>
					</div>
				</div>
			</div>
		</div>
	</div>
	<Prestations />
	<About />
	<Payment />
	<FAQ />
	<!-- <Reviews /> -->
</div>