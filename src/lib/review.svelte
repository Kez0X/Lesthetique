<script>
	// Liste des 10 meilleurs avis
	export let reviews = [
		{
			name: "Aline",
			comment: "Superbe prestation Alexandrine et Anaïs sont très professionnelles et efficaces merci à elles.",
			rating: 5
		},
		{
			name: "Manuela",
			comment: "Anaïs s'est montrée très réactive et rassurante en m'expliquant le déroulement du soin à domicile. On sent le professionnalisme avec du matériel de qualité et des gestes sûrs. Personne très agréable et à l'écoute. Finition de l'épilation à la pince pour un rendu parfait. Je recommande !",
			rating: 5
		},
		{
			name: "Christiane",
			comment: "Les 2 esthéticiennes sont très professionnelles et s'adaptent à l'environnement de leur cliente. Les soins se déroulent comme en institut.",
			rating: 5
		},
		{
			name: "annese",
			comment: "Alexandrine est rassurante et méticuleuse. C'est agréable de se faire chouchouter à domicile.",
			rating: 5
		},
		{
			name: "Camille M.",
			comment: "Ponctuelle, souriante et efficace ! Merci encore 😊",
			rating: 5
		},
		{
			name: "Julie R.",
			comment: "Moment très agréable. Alexandrine est à l'écoute et le massage était top.",
			rating: 5
		},
		{
			name: "Sophie L.",
			comment: "Anaïs est douce et très professionnelle. Je suis ravie de ma manucure !",
			rating: 5
		},
		{
			name: "Isabelle B.",
			comment: "Toujours agréable de passer un moment pour soi et d'avoir des conseils.",
			rating: 5
		},
		{
			name: "Beatrice M.",
			comment: "Prestations de qualité, Rachel est compétente et disponible et prodigue d’excellents conseils sans inciter à la vente.",
			rating: 5
		}
	];
</script>

<div class="reviews-section">
	<h2>NOS MEILLEURS AVIS TREATWELL ⭐</h2>
	<div class="reviews-grid">
		{#each reviews as review}
			<div class="review-card">
				<div class="stars">
					{#each Array(review.rating) as _, i}
						<span>⭐</span>
					{/each}
				</div>
				<p class="comment">"{review.comment}"</p>
				<p class="author">— {review.name}</p>
			</div>
		{/each}
	</div>
	<a class="treatwell-link" href="https://www.treatwell.fr/salon/l-esthetique-aa-estheticiennes-a-domicile/" target="_blank" rel="noopener noreferrer">
		<b>Consulter tous les avis sur Treatwell</b>
	</a>
</div>

<style>
	.reviews-section {
		background: #ffffff;
		padding: 50px 20px;
		text-align: center;
	}

	h2 {
		font-size: 2rem;
		margin-bottom: 30px;
		color: #000000;
	}

	.reviews-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
		gap: 20px;
		max-width: 1000px;
		margin: 0 auto;
	}

	.review-card {
		background: #ffffff;
		border-radius: 12px;
		padding: 20px;
		box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
		transition: transform 0.2s;
	}

	.review-card:hover {
		transform: translateY(-5px);
	}

	.stars {
		color: #ffc107;
		margin-bottom: 10px;
	}

	.comment {
		font-style: italic;
		color: #444;
		margin-bottom: 10px;
	}

	.author {
		color: #777;
		font-size: 0.9em;
	}

	.treatwell-link {
		display: inline-block;
		margin-top: 30px;
		padding: 10px 20px;
		background-color: #ff7f7f;
		color: #fff;
		text-decoration: none;
		border-radius: 5px;
		transition: background-color 0.3s;
	}

	.treatwell-link:hover {
		background-color: #ff5a5a;
	}
</style>
