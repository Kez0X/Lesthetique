<script>
	export let text = "🌸 -15% premier rendez-vous soin visage ou épilation jusqu'au 26 juillet 🌸";
</script>

<div class="promo-banner">
	{text}
</div>

<style>
	.promo-banner {
		position: fixed;
		bottom: 0;
		left: 0;
		width: 100%;
		background-color: #ffffff;
		color: #721c24;
		text-align: center;
		font-weight: bold;
		padding: 10px 15px;
		font-size: 1em;
		z-index: 1000;
	}

	@media (max-width: 768px) {
		.promo-banner {
			font-size: 0.9em;
			padding: 8px 10px;
		}
	}
</style>
