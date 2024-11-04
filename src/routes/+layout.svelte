<script>
	import '../app.css';
	import Navbar from '$lib/navbar.svelte';
	import Prestations from '$lib/prestations.svelte';
	import About from '$lib/about.svelte';
	import Payment from '$lib/payment.svelte';
	import FAQ from '$lib/faq.svelte';
	import Footer from '$lib/footer.svelte';
	import Reviews from '$lib/review.svelte';
	
	// Import de `page` depuis SvelteKit
	import { page } from '$app/stores';
	
	// Création d’une variable réactive `isContactPage`
	$: isContactPage = $page.url.pathname === '/contact';
</script>

<div class="app">
	<Navbar />
	
	<!-- Affiche le contenu principal seulement si ce n’est pas la page de contact -->
	{#if !isContactPage}
		<!-- Page d'accueil -->
		<div class="home-page-container">
			<div class="page-container">
				<slot />
			</div>
		</div>

		<Prestations />
		<About />
		<Payment />
		<FAQ />
		<Reviews />
		<Footer />
	{/if}

	<!-- Affiche le slot uniquement pour la page de contact -->
	{#if isContactPage}
		<div class="contact-page-container">
			<slot />
		</div>
	{/if}
</div>
