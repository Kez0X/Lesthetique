<svelte:head>
	<title>L'esthétique</title>
	<meta name="description" content="" />
</svelte:head>

<script>
	import Instagram from '$lib/images/Instagram.webp';
	import Facebook from '$lib/images/Facebook.png';
</script>

<div class="container">
	<div class="content">
		<h1>L'esthétique by Anaïs</h1>
		<p class="tagline">Beauté à domicile, douceur à chaque instant</p>
		<p class="description">Massages, épilations, onglerie à domicile pour femmes</p>
		<button class="construction-btn"><b>En construction ✨</b></button>
		<p class="follow-us">Nous suivre sur les réseaux sociaux</p>
		<div class="social-icons">
			<a href=""><img src={Facebook} alt="Facebook"></a>
			<a href=""><img src={Instagram} alt="Instagram"></a>
		</div>
	</div>
</div>

<style>
	
</style>
