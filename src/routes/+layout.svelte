<script>
	import Navbar from '$lib/navbar.svelte';
	import Promotion from '$lib/promotion.svelte';
	import Footer from '$lib/footer.svelte';
	import { injectAnalytics } from '@vercel/analytics/sveltekit';
	import '../app.css';

	injectAnalytics();
</script>

<div class="app">
	<Navbar />
	<slot />
	<Footer />
	<Promotion />
</div>
