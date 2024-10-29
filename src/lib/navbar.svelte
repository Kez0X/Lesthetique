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

	<!-- Fond sombre qui couvre toute la page lorsque le menu est ouvert -->
	{#if isMenuOpen}
		<div class="menu-overlay" on:click={toggleMenu}></div>
	{/if}

	<!-- Menu déroulant (slide-in) -->
	<div class="menu-content {isMenuOpen ? 'show' : ''}">
		<div class="menu-close" on:click={toggleMenu}>✕</div>
		<h1>L'esthétiqueAA</h1>

		<!-- Catégories avec images de fond -->
		<div class="menu-item" style="background-image: url('/src/lib/images/onglerie.png');">Onglerie</div>
		<div class="menu-item" style="background-image: url('/src/lib/images/epilations.png');">Épilations</div>
		<div class="menu-item" style="background-image: url('/src/lib/images/massages.png');">Massages</div>
		<div class="menu-item" style="background-image: url('/src/lib/images/soins-visages.png');">Soins Visages</div>
		<div class="menu-item" style="background-image: url('/src/lib/images/rehaussement-cils.png');">Réhaussement de Cils</div>
		<div class="menu-item" style="background-image: url('/src/lib/images/forfaits.png');">Forfaits</div>

		<!-- Lien de contact direct en bas du menu -->
		<div class="contact-estheticiennes">
			<a href="#">Contacter les esthéticiennes</a>
		</div>
	</div>
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
		gap: 40px;
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

	/* Fond sombre couvrant toute la page lors de l’ouverture du menu */
	.menu-overlay {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.4);
		z-index: 9;
	}

	/* Menu latéral glissant depuis la droite */
	.menu-content {
		position: fixed;
		top: 0;
		right: 0;
		width: 80%;
		max-width: 400px;
		height: 100%;
		background-color: #fff;
		box-shadow: -5px 0 15px rgba(0, 0, 0, 0.3);
		z-index: 10;
		padding: 20px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 15px;
		transform: translateX(100%); /* Cacher le menu hors de l’écran par défaut */
		transition: transform 0.3s ease;
	}

	/* Affiche le menu en glissant */
	.menu-content.show {
		transform: translateX(0);
	}

	.menu-close {
		align-self: flex-end;
		font-size: 1.5em;
		cursor: pointer;
	}

	.menu-item {
		width: 100%;
		height: 80px;
		background-size: cover;
		background-position: center;
		color: #fff;
		font-size: 1.2em;
		font-weight: bold;
		display: flex;
		align-items: center;
		justify-content: center;
		text-shadow: 0px 0px 10px rgba(0, 0, 0, 0.7);
		cursor: pointer;
	}

	.contact-estheticiennes {
		margin-top: auto;
		font-size: 1.2em;
		font-weight: bold;
	}

	.contact-estheticiennes a {
		color: #333;
		text-decoration: none;
	}

	/* Styles pour les petits écrans (mobile) */
	@media (max-width: 768px) {
		.menu-content {
			width: 100%; /* Prend toute la largeur sur mobile */
		}
	}
</style>
