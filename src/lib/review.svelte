<script>
    import { onMount } from "svelte";
    import { writable } from "svelte/store";

    let reviews = writable([
        { id: 1, name: "Alice", rating: 5, comment: "Service impeccable, je recommande !" },
        { id: 2, name: "Bob", rating: 4, comment: "Très satisfaite, à refaire." },
        // Ajoute d'autres avis pour la démonstration
        { id: 3, name: "Charlie", rating: 3, comment: "C'était correct." },
        { id: 4, name: "Diana", rating: 5, comment: "Un service exceptionnel." },
        { id: 5, name: "Ethan", rating: 2, comment: "Pas terrible." },
        { id: 6, name: "Fiona", rating: 4, comment: "Très bon rapport qualité/prix." }
    ]);

    let newRating = 0;
    let newComment = "";
    let newName = "";

    function addReview() {
        if (newRating > 0 && newComment.trim() && newName.trim()) {
            reviews.update(currentReviews => [
                ...currentReviews,
                {
                    id: Date.now(),
                    name: newName,
                    rating: newRating,
                    comment: newComment,
                }
            ]);
            newRating = 0;
            newComment = "";
            newName = "";
        }
    }

    // Fonction pour obtenir les 5 meilleurs avis
    $: topReviews = $reviews
        .slice()
        .sort((a, b) => b.rating - a.rating)
        .slice(0, 5); // Limite à 5 avis
</script>

<div class="reviews-section">
    <h2>Ce que disent nos clients ✨</h2>

    {#each topReviews as review}
        <div class="review-card">
            <div class="review-author">{review.name}</div>
            <div class="review-rating">{"⭐".repeat(review.rating)}</div>
            <p>{review.comment}</p>
        </div>
    {/each}

    <div class="add-review">
        <h3>Laissez votre avis</h3>
        <input
            type="text"
            placeholder="Votre nom"
            bind:value={newName}
            required
            style="margin-bottom: 10px; padding: 10px; width: 100%; border-radius: 5px; border: 1px solid #ddd;"
        />

        <div class="rating-stars">
            {#each Array(5) as _, i}
                <span
                    class="star {i < newRating ? '' : 'inactive'}"
                    on:click={() => (newRating = i + 1)}
                >★</span>
            {/each}
        </div>

        <textarea
            placeholder="Votre avis"
            bind:value={newComment}
            rows="4"
            style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid #ddd; resize: none;"
            required
        ></textarea>

        <button class="submit-btn" on:click={addReview}>Envoyer</button>
    </div>
</div>


<style>
    .reviews-section {
        background: linear-gradient(to bottom, #f8f8f8, #ffebf0);
        padding: 60px;
        max-width: 800px;
        margin: 0 auto;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        text-align: center;
    }

    .review-card {
        background-color: #fff;
        border-radius: 8px;
        padding: 20px;
        margin-bottom: 20px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s;
    }

    .review-card:hover {
        transform: scale(1.02);
    }

    .review-author {
        font-weight: bold;
        color: #333;
    }

    .review-rating {
        color: #ff5a5a;
        font-size: 1.2em;
    }

    .add-review {
        margin-top: 40px;
        padding: 20px;
        background-color: #fff;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    .rating-stars {
        display: flex;
        gap: 5px;
        cursor: pointer;
        justify-content: center;
        margin-bottom: 10px;
    }

    .star {
        font-size: 1.5em;
        color: #ff5a5a;
    }

    .star.inactive {
        color: #ccc;
    }

    button.submit-btn {
        background-color: #ff7f7f;
        color: #fff;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    button.submit-btn:hover {
        background-color: #ff5a5a;
    }
</style>