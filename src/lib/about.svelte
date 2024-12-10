<script>
    import OullinsMetro from '$lib/images/8570_671_Inauguration-Oullins-St-Genis-Laval-51 1.png';
    import OullinsMairie from '$lib/images/implanter2 1.png';
    import SalonCoiffure from '$lib/images/u9lyuns3drewo1gj5p8m 1.png';
</script>

<div class="section-about">
    <h2>À PROPOS DE NOUS</h2>
    <p>Nous sommes 2 esthéticiennes indépendantes qui se sont lancées en décembre 2024, dans le but de répondre au mieux aux besoins de leur clientèle. C’est pourquoi nous ferons toujours de notre mieux pour vous faire passer le meilleur moment.</p>
    <div class="estheticiennes">
        <div class="estheticienne-description">
            <h3>Anaïs</h3>
            <p>Étant diplômée du CAP, BP et BTS esthétique avec plus de 7 ans d’expérience dans
                le domaine, j'ai décidé avec ma collaboratrice d’ouvrir notre entreprise pour vous offrir des soins personnalisés avec
                des produits et méthodes respectueuses de votre peau. Nous prenons le temps de comprendre
                vos besoins pour vous garantir satisfaction et détente. Hâte de vous rencontrer pour
                partager ce moment beauté avec vous !</p>
            <button class="construction-btn" on:click={() => window.location.href = '/contact'}><b>Prendre rendez-vous 😊</b></button>
            <p class="description">Paiement au début de la scéance -
                (cartes ou espèces, pas de chèques) -
                Réservé uniquement aux femmes</p>
        </div>
        <div class="estheticienne-description">
            <h3>Alexandrine</h3>
            <p>Esthéticienne depuis plus de 2 ans, je suis passionnée par la beauté et le bien-être. Notre objectif est de vous offrir des soins personnalisés pour un moment de détente inoubliable. Que ce soit pour des épilations, des soins du visage ou des manucures, nous mettons tout en œuvre pour répondre à vos attentes. Hâte de vous accueillir et de partager ce moment de beauté avec vous !</p>
            <button class="construction-btn" on:click={() => window.location.href = '/contact'}><b>Prendre rendez-vous 😊</b></button>
            <p class="description">Paiement au début de la scéance -
            (cartes ou espèces, pas de chèques) -
            Réservé uniquement aux femmes</p>
        </div>
    </div>
    <div class="image-section">
        <div class="image-with-description">
            <img alt="Image du métro d'Oullins" src={OullinsMetro}/>
            <p>Nous avons décidé de nous déplacer à domicile afin de répondre à une demande de gain de
                temps et d’adaptabilité, tout en recréant l’ambiance relaxante et cocooning d’un institut de
                beauté au sein de chez vous.</p>
        </div>

        <div class="image-with-description">
            <img alt="Image de la mairie d'Oullins" src={OullinsMairie}/>
            <p>Oullins était une évidence, car c’est là où tout a commencé pour nous professionnellement.
                Nous avions donc déjà des liens privilégiés avec les commerçants ainsi qu’avec les
                habitants de la commune. C’est également un point central pour les autres villes où nous
                proposons nos services.</p>
        </div>

        <div class="image-with-description">
            <img alt="Image de notre salon de coiffure partenaire" src={SalonCoiffure}/>
            <p>Vous pouvez nous retrouver au sein du salon de coiffure Line’s Coiffure, situé au 11 bis
                boulevard de l’Europe à Oullins, afin de réaliser : les épilations du visage sans autres
                prestations, les soins des mains et la pose de vernis semi-permanent.
                Accessible en transport en commun ou stationnement libre et gratuit au sein de la résidence.</p>
        </div>
    </div>

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
        width: 75%; /* Augmentation de la largeur du paragraphe */
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

    .image-section {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 30px;
        padding : 30px;
    }

    .image-with-description {
        display: flex;
        align-items: center;
        gap: 20px;
        width: 60%;
        background: #ffffff;
        border-radius: 15px;
        padding: 20px;
        box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        text-align: left;
    }

    .image-with-description img {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        object-fit: cover;
        box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    }

    .image-with-description p {
        margin: 0;
        color: #666;
        line-height: 1.4;
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
        .section-about p, .image-with-description {
            width: 90%;
        }

        .image-with-description {
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .image-with-description img {
            margin-bottom: 15px;
        }
    }
</style>