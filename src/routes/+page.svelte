<svelte:head>
	<title>L'esthétique - Accueil</title>
	<meta name="description" content="" />
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
					<button class="construction-btn" on:click={() => window.location.href = '/contact'}>
						<b>Prendre rendez-vous sur planity 💻</b>
					</button>
					<p class="follow-us-localisation">Notre secteur d'activité : Oullins, Saint-Genis-Laval, Sainte-Foy-lès-Lyon, La Mulatière, Tassin,
						Craponne, Millery, Charly, Vernaison, Irigny, Brignais,
						Chaponost, Pierre-bénite</p>
					<p class="follow-us" style="margin-top : 5px">Nous suivre sur les réseaux sociaux</p>
					<div class="social-icons">
						<a href="https://www.facebook.com/profile.php?id=61563897359229"><img src={Facebook} alt="Facebook"></a>
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
	<Reviews />
</div>
