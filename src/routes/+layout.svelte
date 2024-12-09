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
