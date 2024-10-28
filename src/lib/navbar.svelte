<script>
	import Logo from '$lib/images/favicon.jpg';
	let isMenuOpen = false;

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}
</script>

<div class="navbar">
	<div class="navbar-container">
		<!-- Logo à gauche -->
		<div class="logo">
			<a href="#"><img src={Logo} alt="logo"></a>
		</div>

		<!-- Menu et contact à droite -->
		<div class="right">
			<!-- Lien de contact -->
			<div class="contact">
				<a href="#">Nous contacter</a>
			</div>
			<!-- Bouton de menu toujours visible -->
			<div class="menu-button" on:click={toggleMenu}>
				<span>☰</span>
			</div>
		</div>
	</div>

	<!-- Menu déroulant (slide-in) -->
	{#if isMenuOpen}
	<div class="menu-overlay" on:click={toggleMenu}></div>
	<div class="menu-content">
		<div class="menu-close" on:click={toggleMenu}>✕</div>
		<h1>L'esthétique by Anaïs & Alexandrine</h1>
		<div class="menu-item">Onglerie</div>
		<div class="menu-item">Épilations</div>
		<div class="menu-item">Massages</div>
		<div class="menu-item">Soins Visages</div>
		<div class="menu-item">Réhaussement de Cils</div>
		<div class="menu-item">Forfaits</div>
	</div>
	{/if}
</div>

<style>
	/* Styles généraux de la navbar */
	.navbar {
		width: 100%;
		height: 80px;
		background-color: rgba(255, 255, 255, 0.904);
		position: sticky;
		top: 0;
		box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
		z-index: 10;
		display: flex;
		align-items: center;
		justify-content: center;
	}

    .container {
        background-color: rgba(255, 255, 255, 0.8);
    }

	.navbar-container {
		width: 100%;
		max-width: 1200px;
		padding: 0 20px;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	/* Logo à gauche */
	.logo img {
		height: 70px;
	}

	/* Bouton de menu et contact à droite */
	.right {
		display: flex;
		align-items: center;
		gap: 20px;
	}

	.contact a {
		text-decoration: none;
		color: #333;
		font-weight: bold;
		font-size: 1em;
	}

	/* Toujours visible, même sur grands écrans */
	.menu-button {
		font-size: 1.5em;
		cursor: pointer;
	}

	/* Menu déroulant pour tous les écrans */
	.menu-overlay {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.4);
		z-index: 9;
	}

	.menu-content {
		position: fixed;
		top: 0;
		right: 0;
		width: 80%;
		max-width: 300px;
		height: 100%;
		background-color: #fff;
		box-shadow: -5px 0 15px rgba(0, 0, 0, 0.3);
		z-index: 10;
		padding: 20px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 15px;
		transform: translateX(100%);
		transition: transform 0.3s ease;
	}

	.menu-content.show {
		transform: translateX(0);
	}

	.menu-close {
		align-self: flex-end;
		font-size: 1.5em;
		cursor: pointer;
	}

	.menu-item {
		font-size: 1.2em;
		font-weight: bold;
		padding: 10px 0;
		cursor: pointer;
	}

	/* Responsive Styles */
	@media (max-width: 768px) {
		.contact a {
			font-size: 0.9em;
		}

		/* Ajustements du conteneur */
		.container {
			padding: 0 15px;
		}
	}
</style>
