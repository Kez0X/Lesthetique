<svelte:head>
	<title>L'esthétique</title>
	<meta name="description" content="" />
</svelte:head>

<script>
	import Instagram from '$lib/images/Instagram.webp';
	import Facebook from '$lib/images/Facebook.png';
	import Brochure from '$lib/images/Beige Organic Beauty and Spa Brochure.pdf';
</script>

<div class="container">
	<div class="content">
		<h1>L'esthétiqueAA</h1>
		<p class="tagline">Beauté à domicile, douceur à chaque instant</p>
		<p class="description">Massages, épilations, onglerie à domicile pour femmes</p>
		<button class="construction-btn"><b>En construction ✨</b></button>
		<p class="follow-us">Notre secteur d'activité : Oullins, Pierre Bénite, La Mulatière</p>
		<button on:click={() => window.location.href = Brochure} class="construction-btn"><b>Nos prestations 💄</b></button>
		<p class="follow-us">Nous suivre sur les réseaux sociaux</p>
		<div class="social-icons">
			<a href="https://www.facebook.com/share/ckJ3a91v4Mo9PtRF/"><img src={Facebook} alt="Facebook"></a>
			<a href="https://www.instagram.com/anaisdelice.estheticienne69?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw=="><img src={Instagram} alt="Instagram"></a>
		</div>
	</div>
</div>

<style>
	
</style>
