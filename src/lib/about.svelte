<div class="section-about">
    <h2>À PROPOS DE NOUS</h2>
    <p>Nous sommes 2 esthéticiennes indépendantes qui se sont lancés en janvier 2025, dans le but de répondre au mieux aux besoins de leurs clientèle. C’est pourquoi nous ferons toujours de notre mieux pour vous faire passer le meilleur moment.</p>
    <div class="estheticiennes">
        <div class="estheticienne-description">
            <h3>Anaïs</h3>
            <p>Esthéticienne depuis plus de 7 ans, expérimentée, profitez de ses différents massages et épilations pour passer un bon moment.</p>
            <button class="construction-btn"><b>Prendre rendez-vous 😄</b></button>
            <p class="description">Paiement au début de la scéance -
                (cartes ou espèces, pas de chèques) -
                Réservé uniquement aux femmes</p>
        </div>
        <div class="estheticienne-description">
            <h3>Alexandrine</h3>
            <p>Esthéticienne depuis plus de 2 ans, profitez de ses talents d’esthéticienne pour passer un bon moment, et profitez aussi de ses talents artistiques pour vos ongles.</p>
            <button class="construction-btn"><b>Prendre rendez-vous 😊</b></button>
            <p class="description">Paiement au début de la scéance -
            (cartes ou espèces, pas de chèques) -
            Réservé uniquement aux femmes</p>
        </div>
    </div>
    <p class="image-description">Après avoir écouté nos clients et c’est pourquoi au lieu de leur demander de se déplacer, nous nous déplacons directement à domicile afin de leur économiser le maximum de temps. Un entreprise à domicile basé à Oullins pour vous correspondre au mieux.</p>
</div>


<style>
    /* Styles pour la section globale */
    .section-about {
        width: 100%;
        text-align: center;
        padding: 50px 20px; /* Ajout de padding latéral */
        background-color: #f8f8f8;
    }

    .section-about h2 {
        font-size: 2em; /* Augmentation de la taille du titre */
        margin-bottom: 20px;
        color: #333;
    }

    .section-about p {
        width: 60%; /* Augmentation de la largeur du paragraphe */
        margin: 0 auto 30px auto; /* Centrer et espacer le paragraphe */
        line-height: 1.6; /* Amélioration de l'espacement entre les lignes */
        color: #555; /* Couleur du texte */
    }

    /* Styles pour les descriptions des esthéticiennes */
    .estheticiennes {
        display: flex;
        justify-content: center; /* Centrer les descriptions */
        flex-wrap: wrap; /* Permet aux éléments de passer à la ligne sur les petits écrans */
        gap: 20px; /* Espace entre les cartes */
    }

    .estheticienne-description {
        background: white;
        border-radius: 10px; /* Coins arrondis */
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Ombre légère */
        padding: 20px; /* Espacement interne */
        width: 350px; /* Largeur fixe pour chaque description */
        margin: 10px; /* Espacement externe */
        transition: transform 0.3s; /* Animation lors du survol */
    }

    .estheticienne-description:hover {
        transform: translateY(-5px); /* Légère élévation au survol */
    }

    .estheticienne-description h3 {
        font-size: 1.8em; /* Taille de la police du nom */
        margin-bottom: 10px;
        color: #ff7f7f; /* Couleur du nom */
    }

    .estheticienne-description p {
        margin-bottom: 15px; /* Espacement entre les paragraphes */
        color: #666; /* Couleur pour le texte des descriptions */
    }

    .estheticienne-description .description {
        font-family: 'Crimson Text', sans-serif;
        font-size : 0.9em;
    }

    .section-about .image-description{
        padding : 10px;
    }

    /* Responsive design */
    @media (max-width: 768px) {
        .section-about p {
            width: 90%; /* Réduire la largeur sur les petits écrans */
        }
        .estheticienne-description {
            width: 100%; /* Occupation de toute la largeur sur les petits écrans */
            margin: 10px 0; /* Ajuster l'espacement pour les petits écrans */
        }
    }
</style>