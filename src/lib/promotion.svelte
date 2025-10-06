<script>
	export let text = "🌸🍂 Profitez de l'automne pour prendre soin de vous ! 🍂🌸 Découvrez nos soins du visage, massages relaxants et prestations beauté pour un automne tout en douceur. 🍁✨ Prenez rendez-vous dès aujourd’hui et offrez-vous un moment de bien-être ! 🌸";
</script>

<div class="promo-banner">
	<div class="scrolling-text">{text}</div>
</div>

<style>
	.promo-banner {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		background-color: #f5c6cb;
		color: #721c24;
		text-align: center;
		font-weight: bold;
		padding: 10px 15px;
		font-size: 1em;
		overflow: hidden;
		z-index: 1000;
        max-height : 42px;
	}

	.scrolling-text {
		display: inline-block;
		white-space: nowrap;
		animation: scroll-left 20s linear infinite;
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
			font-size: 0.9em;
            height : 100%;
		}
	}
</style>
