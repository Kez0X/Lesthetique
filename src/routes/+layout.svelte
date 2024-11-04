<script>
	import '../app.css';
	import Navbar from '$lib/navbar.svelte';
	import Prestations from '$lib/prestations.svelte';
	import About from '$lib/about.svelte';
	import Payment from '$lib/payment.svelte';
	import FAQ from '$lib/faq.svelte';
	import Footer from '$lib/footer.svelte';
</script>
<div class="app">
	<!-- <Header /> -->
	<Navbar />
	<div class="home-page-container">
		<div class="page-container">
			<slot />
		</div>
	</div>
	<Prestations/>
	<About/>
	<Payment/>
	<FAQ/>
	<Footer/>
	<!-- <footer>
		<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
	</footer> -->
</div>
