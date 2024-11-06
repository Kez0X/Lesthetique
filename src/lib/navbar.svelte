<script>
	import Instagram from '$lib/images/Instagram.webp';
	import Facebook from '$lib/images/Facebook.png';
	import Logo from '$lib/images/favicon.jpg';
	import Onglerie from '$lib/images/onglerie.png';
	import Epilations from '$lib/images/epilations.png';
	import Massages from '$lib/images/massages.png';
	import Rehaussement from '$lib/images/rehaussement-cils.png';
	import Soins from '$lib/images/soins-visages.png';
	import Forfaits from '$lib/images/forfaits.png';

	let isMenuOpen = false;

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}
</script>

<div class="navbar">
	<div class="navbar-container">
		<!-- Logo à gauche -->
		<div class="logo">
			<a href="/"><img src={Logo} alt="logo"></a>
		</div>

		<!-- Menu et contact à droite -->
		<div class="right">
			<!-- Lien de contact -->
			<div class="contact">
				<a href="/contact">Nous contacter</a>
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

		<!-- Catégories avec images de fond, rendant chaque élément cliquable -->
		<a href="/onglerie" class="menu-item" style="background-image: url({Onglerie});" on:click={toggleMenu}>
			<div class="menu-item-back">Onglerie</div>
		</a>
		<a href="/epilations" class="menu-item" style="background-image: url({Epilations});" on:click={toggleMenu}>
			<div class="menu-item-back">Épilations</div>
		</a>
		<a href="/soins-corps" class="menu-item" style="background-image: url({Massages});" on:click={toggleMenu}>
			<div class="menu-item-back">Soins Corps</div>
		</a>
		<a href="/soins-visage" class="menu-item" style="background-image: url({Soins});" on:click={toggleMenu}>
			<div class="menu-item-back">Soins Visages</div>
		</a>
		<a href="/rehaussement-cils" class="menu-item" style="background-image: url({Rehaussement});" on:click={toggleMenu}>
			<div class="menu-item-back">Réhaussement de Cils</div>
		</a>
		<a href="/forfaits" class="menu-item" style="background-image: url({Forfaits});" on:click={toggleMenu}>
			<div class="menu-item-back">Forfaits</div>
		</a>

		<!-- Lien de contact direct en bas du menu -->
		<div class="contact-estheticiennes">
			<div class="social-icons">
				<a href=""><img src={Facebook} alt="Facebook"></a>
				<a href="https://www.instagram.com/anaisdelice.estheticienne69?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw==">
					<img src={Instagram} alt="Instagram">
				</a>
			</div>
			<a href="/contact" on:click={toggleMenu}>Contacter les esthéticiennes</a>
		</div>
	</div>
</div>

<style>
	/* Styles généraux de la navbar */
	.navbar {
		width: 100%;
		height: 70px;
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
		height: 50px;
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
		transform: translateX(100%);
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
		position: relative;
		width: 100%;
		height: 80px;
		background-size: cover;
		background-position: center;
		display: flex;
		align-items: center;
		justify-content: center;
		color: #fff;
		font-size: 1.2em;
		font-weight: bold;
		cursor: pointer;
		text-decoration: none;
		color: inherit;
		overflow: hidden;
		transition: transform 0.3s ease; /* Transition pour le zoom */
	}

	/* Overlay assombrissant au survol avec ::before */
	.menu-item::before {
		content: "";
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.4);
		transition: background-color 0.3s ease;
		z-index: 1;
	}

	/* Contenu du texte au-dessus de l'overlay */
	.menu-item-back {
		position: relative;
		z-index: 2;
		background-color: rgba(255, 255, 255, 0.8);
		border-radius: 5px;
		padding: 5px 20px;
		text-align: center;
	}

	/* Effets de zoom et assombrissement lors du survol */
	.menu-item:hover {
		transform: scale(1.05); /* Zoom sur l'élément */
	}

	.menu-item:hover::before {
		background-color: rgba(0, 0, 0, 0.6); /* Assombrissement plus intense */
	}

	.contact-estheticiennes {
		margin-top: auto;
		font-size: 1.2em;
		font-weight: bold;
	}

	.social-icons {
		justify-items: center;
		text-align: center;
		padding-bottom: 10px;
	}

	.social-icons a {
		margin: 0 10px;
	}

	.social-icons img {
		width: 40px;
	}

	.contact-estheticiennes a {
		color: #333;
		text-decoration: underline;
	}

	/* Styles pour les petits écrans (mobile) */
	@media (max-width: 768px) {
		.menu-content {
			width: 100%;
		}
	}
</style>
