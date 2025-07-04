<script>
	export let text = "🌸 -15% premier rendez-vous soin visage ou épilation jusqu'au 26 juillet 🌸";
</script>

<div class="promo-banner">
	<div class="scrolling-text">{text}</div>
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
		overflow: hidden;
		z-index: 1000;
	}

	.scrolling-text {
		display: inline-block;
		white-space: nowrap;
		animation: scroll-left 15s linear infinite;
	}

	@keyframes scroll-left {
		0% {
			transform: translateX(100%);
		}
		100% {
			transform: translateX(-100%);
		}
	}

	@media (max-width: 768px) {
		.promo-banner {
			background-color: #f5c6cb;
			font-size: 0.9em;
			padding: 10px 10px;
		}
	}
</style>
