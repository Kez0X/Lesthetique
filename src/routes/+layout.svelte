<script>
	import '../app.css';
	import { injectAnalytics } from '@vercel/analytics/sveltekit'
	import Navbar from '$lib/navbar.svelte';
	import Footer from '$lib/footer.svelte';	
</script>

<div class="app">
	<Navbar />
	<slot />
	<Footer />
</div>
