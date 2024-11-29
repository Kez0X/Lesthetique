<script>
    import { onMount } from "svelte";

    // Stockage des avis
    let reviews = [];
    let isLoading = true; // Indicateur de chargement

    // Fonction pour récupérer les avis depuis l'API Planity
    async function fetchReviews() {
        try {
            const response = await fetch("https://api.planity.com/reviews"); // URL d'exemple, à adapter
            if (response.ok) {
                const data = await response.json();
                reviews = data.reviews || []; // Adaptez selon la structure des données
            } else {
                console.error("Erreur lors de la récupération des avis Planity :", response.status);
            }
        } catch (error) {
            console.error("Impossible de récupérer les avis :", error);
        } finally {
            isLoading = false;
        }
    }

    // Charger les avis lors du montage du composant
    onMount(() => {
        fetchReviews();
    });

    // Fonction pour rediriger vers la page Planity
    function bookAppointment() {
        window.open("https://www.planity.com", "_blank");
    }
</script>

<div class="reviews-section">
    <h2>Ce que disent nos clients 🌸</h2>

    {#if isLoading}
        <p>Chargement des avis...</p>
    {:else if reviews.length === 0}
        <p>Aucun avis à afficher.</p>
    {:else}
        <div class="grid-container">
            {#each reviews as review}
                <div class="review-card">
                    <div class="review-author">{review.authorName}</div>
                    <div class="review-rating">{"⭐".repeat(review.rating)}</div>
                    <p>{review.comment}</p>
                </div>
            {/each}
        </div>
    {/if}

    <button class="button" on:click={bookAppointment}>
        Prendre rendez-vous sur Planity
    </button>
</div>

<style>
    .reviews-section {
        background-color: #f8f8f8;
        padding: 50px 0;
        text-align: center;
    }

    h2 {
        font-size: 2em;
        margin-bottom: 30px;
        color: #333;
    }

    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 20px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .review-card {
        position: relative;
        background-color: white;
        border-radius: 15px;
        padding: 20px;
        box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.15);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .review-card:hover {
        transform: scale(1.03);
        box-shadow: 0px 15px 30px rgba(0, 0, 0, 0.2);
    }

    .review-author {
        font-weight: bold;
        color: #333;
        margin-bottom: 10px;
    }

    .review-rating {
        color: #ff7f7f;
        font-size: 1.2em;
        margin-bottom: 10px;
    }

    .button {
        display: inline-block;
        padding: 10px 20px;
        background-color: #ff7f7f;
        color: white;
        border-radius: 5px;
        text-align: center;
        font-weight: bold;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    .button:hover {
        background-color: #ff5a5a;
    }

    p {
        color: #555;
        font-size: 1em;
        margin-top: 20px;
    }
</style>
