<script>
	import onglerie from '$lib/images/onglerie.png';
	import epilations from '$lib/images/epilations.png';
	import massages from '$lib/images/massages.png';
	import soinsVisages from '$lib/images/soins-visages.png';
	import rehaussementCils from '$lib/images/rehaussement-cils.png';
	import forfaits from '$lib/images/forfaits.png';
	import maquillage from '$lib/images/maquillage.webp';

	let categories = [
	   {
		  title: "ONGLERIE",
		  backgroundImage: onglerie,
		  link: "/onglerie",
		  prestations: [
			 { name: "Pose de vernis semi-permanent", price: "40€" },
			 { name: "Soin des mains", price: "50€" },
			 { name: "Soin des pieds", price: "55€" }
		  ]
	   },
	   {
		  title: "ÉPILATIONS",
		  backgroundImage: epilations,
		  link: "/epilations",
		  prestations: [
			 { name: "Sourcils", price: "14€" },
			 { name: "Maillot complet", price: "28€" },
			 { name: "Jambes complètes, complet, aisselles", price: "67€" }
		  ]
	   },
	   {
		  title: "SOINS CORPS",
		  backgroundImage: massages,
		  link: "/soins-corps",
		  prestations: [
			 { name: "Gommage", price: "35€" },
			 { name: "Drainage minceur", price: "50€" },
			 { name: "Relaxant", price: "50€" }
		  ]
	   },
	   {
		  title: "SOINS VISAGES",
		  backgroundImage: soinsVisages,
		  link: "/soins-visage",
		  prestations: [
			 { name: "Nettoyage de peau personnalisé", price: "50€" },
			 { name: "Relaxant 30min", price: "35€" },
			 { name: "Relaxant 1h", price: "50€" }
		  ]
	   },
	   {
		  title: "FORFAITS",
		  backgroundImage: forfaits,
		  link: "/forfaits",
		  prestations: [
			 { name: "Forfait bien être", price: "95€" },
			 { name: "Forfait Spa", price: "125€" },
			 { name: "Forfait beauté des mains", price: "95€" }
		  ]
	   },
	   {
		  title: "MAQUILLAGE",
		  backgroundImage: maquillage,
		  link: "/maquillage",
		  prestations: [
			 { name: "Mariée", price: "80€" },
			 { name: "Maquillage soirée", price: "40€" }
		  ]
	   }
	];
</script>

<div class="section-prestations" id="prestations">
	<h2>NOS PRESTATIONS ✨</h2>
	<div class="grid-container">
		{#each categories as category}
			<a href={category.link} class="category" style="background-image: url({category.backgroundImage})">
				<div class="category-content">
					<div class="category-title">{category.title}</div>
					{#each category.prestations as prestation}
						<div class="prestation">
							<span>{prestation.name}</span>
							<span>{prestation.price}</span>
						</div>
					{/each}
					<a href={category.link} class="button">Voir toutes les prestations</a>
				</div>
			</a>
		{/each}
	</div>
</div>

<style>
	/* Styles pour la section globale */
	.section-prestations {
		width: 100%;
		text-align: center;
		padding: 50px 0;
		background-color: white;
	}

	.section-prestations h2 {
		font-size: 2em;
		margin-bottom: 30px;
		color: #333;
		text-decoration: none;
	}

	/* Disposition en grille pour les catégories */
	.grid-container {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		max-width: 1400px;
		margin: 0 auto;
		gap: 20px;
		padding: 0 5%;
	}

	.category {
		position: relative;
		height: 250px;
		display: flex;
		align-items: center;
		justify-content: center;
		border-radius: 15px;
		overflow: hidden;
		box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.15);
		transition: transform 0.3s ease, box-shadow 0.3s ease;
		background-size: cover;
		background-position: center;
		text-decoration: none;
		color: inherit;
	}

	/* Effet de zoom et ombrage au survol */
	.category:hover {
		transform: scale(1.03);
		box-shadow: 0px 15px 30px rgba(0, 0, 0, 0.2);
	}

	.category::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.3);
		z-index: 1;
	}

	.category-content {
		position: relative;
		z-index: 2;
		background-color: rgba(255, 255, 255, 0.8);
		border-radius: 8px;
		padding: 20px;
		text-align: left;
		width: 80%;
		box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
	}

	.category-title {
		font-size: 1.5em;
		font-weight: bold;
		color: #333;
		margin-bottom: 10px;
	}

	.prestation {
		display: flex;
		justify-content: space-between;
		color: #555;
		font-size: 1em;
		margin: 5px 0;
	}

	.button {
		margin-top: 15px;
		display: inline-block;
		padding: 10px 20px;
		background-color: #ff7f7f;
		color: white;
		text-decoration: none;
		border-radius: 5px;
		font-weight: bold;
		text-align: center;
		transition: background-color 0.3s;
	}

	.button:hover {
		background-color: #ff5a5a;
	}

	/* Retirer les soulignements pour tous les liens */
	a {
		text-decoration: none;
		color: inherit;
	}

	/* Responsive design */
	@media (max-width: 1024px) {
		.grid-container {
			grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
		}
		.category {
			height: 275px;
		}
	}

	@media (max-width: 768px) {
		.category {
			height: 250px;
		}
		.category-title {
			font-size: 1.3em;
		}
		.prestation {
			font-size: 0.9em;
		}
	}
</style>
