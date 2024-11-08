<script>
    // Liste des questions et réponses pour la FAQ
    let faqs = [
        {
            question: "Où vous déplacez vous ?",
            answer: "Nous sommes basés sur Oullins et nous nous déplaçons dans la région sud-ouest lyonnaise : oullins, ste foy-lès-lyon,saint genis laval, tassin, irigny, pierre bénite, la mulatière, charly, vernaison, millery, chaponost, brignais, Craponne",
            open: false
        },
        {
            question: "Vous déplacez vous a domicile pour toutes les prestations ?",
            answer: "Non, les épilations visage sans autres prestations se feront directement au sein du salon Line’s coiffure situé au 11 bis boulevard de l’europe , 69600 oullins.",
            open: false
        },
        {
            question: "Utilisez vous des produits bio et naturels ?",
            answer: "Les épilations sont réalisées avec des cires bio. Les soins du corps sont réalisés avec des produits naturels, huiles végétales. Les soins du visage sont réalisés avec les produits de la marque Clairjoie bio et made in France. Les soins des mains et des pieds sont réalisés avec des produits naturels. Le semi permanent et les réhaussements de cils sont quant à eux réalisés avec des produits conventionnels.",
            open: false
        },
        {
            question: "Quels moyens de paiements acceptez vous ?",
            answer: "Nous acceptons la carte bancaire et les espèces. Les chèques bancaires ne sont pas acceptés, ainsi que les cartes et chèques cadeaux qui ne proviennent pas de chez nous.",
            open: false
        },
        {
            question: "Les mineurs peuvent t-ils prendrent des prestations ?",
            answer: "Tous soins corps, drainage du visage, épilations du maillot intégral et brésilien ainsi que les réhaussements de cils et pose de vernis semi permanent ne sont pas pratiqués sur les mineurs. Les soins du visage et les autres prestations sont quant à elles réalisables avec accord et présence parentale au moment du rdv.",
            open: false
        },
        {
            question: "Quels réglementations pour les femmes enceinte ?",
            answer: "Tous les soins corps ne sont pas pratiqués sur femmes enceinte. Pour les autres prestations pas de contre indications, seuls les soins du visage seront adaptés en conséquence.",
            open: false
        }
    ];

    // Fonction pour basculer l'état d'ouverture d'une FAQ
    function toggleFAQ(index) {
        faqs = faqs.map((faq, i) => i === index ? { ...faq, open: !faq.open } : faq);
    }
</script>

<style>
    .faq-section {
        width: 70%;
        margin: 0 auto;
        text-align: center;
    }

    .faq-section h2 {
        font-size: 1.8em;
        color: #333;
        margin-bottom: 20px;
    }

    .faq-item {
        margin-bottom: 10px;
        border-radius: 8px;
        overflow: hidden;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .faq-question {
        width: 100%;
        padding: 15px;
        font-size: 1.1em;
        font-weight: bold;
        color: #333;
        background-color: #fbcfd1; /* Rose pastel */
        border: none;
        text-align: left;
        cursor: pointer;
        outline: none;
        display: flex;
        justify-content: space-between;
        align-items: center;
        transition: background-color 0.3s ease;
    }

    .faq-question:hover {
        background-color: #f8a5a7;
    }

    /* Chevron plus subtil */
    .faq-question::after {
        content: "⌄"; /* Icône de flèche plus discrète */
        font-size: 1.2em;
        transition: transform 0.3s ease;
    }

    /* Rotation du chevron quand la réponse est visible */
    .faq-item.open .faq-question::after {
        transform: rotate(180deg);
    }

    .faq-answer {
        padding: 15px;
        font-size: 1em;
        color: #555;
        display: none; /* Cachée par défaut */
        background-color: #fde2e4; /* Couleur plus claire pour la réponse */
    }

    /* Affichage de la réponse lorsque l'élément est ouvert */
    .faq-item.open .faq-answer {
        display: block;
    }
</style>

<div class="faq-section">
    <h2>FAQ</h2>
    {#each faqs as faq, index}
        <div class="faq-item {faq.open ? 'open' : ''}">
            <button class="faq-question" on:click={() => toggleFAQ(index)}>
                {faq.question}
            </button>
            {#if faq.open}
                <div class="faq-answer">
                    {faq.answer}
                </div>
            {/if}
        </div>
    {/each}
</div>
