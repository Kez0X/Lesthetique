<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=Material+Icons" rel="stylesheet">
</svelte:head>
<script>
	import Navbar from '$lib/navbar.svelte';
	import Promotion from '$lib/promotion.svelte';
	import Footer from '$lib/footer.svelte';
	import { injectAnalytics } from '@vercel/analytics/sveltekit';
	import '../app.css';

	injectAnalytics();
</script>

<div class="app">
  <Promotion />
	<Navbar />
	<slot />
	<Footer />
</div>
