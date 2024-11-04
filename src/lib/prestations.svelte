<script>
	import onglerie from '$lib/images/onglerie.png';
	import epilations from '$lib/images/epilations.png';
	import massages from '$lib/images/massages.png';
	import soinsVisages from '$lib/images/soins-visages.png';
	import rehaussementCils from '$lib/images/rehaussement-cils.png';
	import forfaits from '$lib/images/forfaits.png';
 
	let categories = [
	   {
		  title: "ONGLERIE",
		  backgroundImage: onglerie,
		  prestations: [
			 { name: "Soin des mains", price: "50€" },
			 { name: "Soin des pieds", price: "55€" },
			 { name: "Prestation complète", price: "105€" }
		  ]
	   },
	   {
		  title: "ÉPILATIONS",
		  backgroundImage: epilations,
		  prestations: [
			 { name: "Forfaits visage complet", price: "45€" },
			 { name: "Maillot complet", price: "28€" },
			 { name: "Jambes complètes, complet, aisselles", price: "67€" }
		  ]
	   },
	   {
		  title: "SOINS CORPS",
		  backgroundImage: massages,
		  prestations: [
			 { name: "Drainage lymphatique ", price: "65€" },
			 { name: "Drainage minceur", price: "75€" },
			 { name: "Relaxant", price: "65€" }
		  ]
	   },
	   {
		  title: "SOINS VISAGES",
		  backgroundImage: soinsVisages,
		  prestations: [
			 { name: "Express", price: "50€" },
			 { name: "Personnalisé", price: "65€" },
			 { name: "Personnalisé anti-age", price: "75€" }
		  ]
	   },
	   {
		  title: "REHAUSSEMENT DE CILS",
		  backgroundImage: rehaussementCils,
		  prestations: [
			 { name: "Avec teinture", price: "50€" },
			 { name: "Sans teinture", price: "45€" },
		  ]
	   },
	   {
		  title: "FORFAITS",
		  backgroundImage: forfaits,
		  prestations: [
			 { name: "Forfaits sourcils lèvres", price: "22€" },
			 { name: "Cure de 6 séances", price: "420€" },
			 { name: "1/2 jambes, complet, aisselles", price: "59€" }
		  ]
	   }
	];
 </script>
 

<style>
	/* Styles pour la section globale */
	.section-prestations {
		width: 100%;
		text-align: center;
		padding: 50px 0;
		background-color: #f8f8f8;
	}

	.section-prestations h2 {
		font-size: 2em;
		margin-bottom: 30px;
		color: #333;
	}

	/* Disposition en grille pour les catégories */
	.grid-container {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Ajuste la largeur de chaque carte */
		max-width: 1400px; /* Limite la largeur totale de la grille */
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
		background-color: rgba(0, 0, 0, 0.3); /* Assombrit l'image */
		z-index: 1;
	}

	.category-content {
		position: relative;
		z-index: 2; /* Au-dessus de l'overlay */
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

<div class="section-prestations" id="prestations">
	<h2>NOS PRESTATIONS</h2>
	<div class="grid-container">
		{#each categories as category}
			<div class="category" style="background-image: url({category.backgroundImage})">
				<div class="category-content">
					<div class="category-title">{category.title}</div>
					{#each category.prestations as prestation}
						<div class="prestation">
							<span>{prestation.name}</span>
							<span>{prestation.price}</span>
						</div>
					{/each}
					<a href="#" class="button">Voir toutes les prestations</a>
				</div>
			</div>
		{/each}
	</div>
</div>
