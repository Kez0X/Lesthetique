<script>
    import OullinsMetro from '$lib/images/8570_671_Inauguration-Oullins-St-Genis-Laval-51 1.png';
    import OullinsMairie from '$lib/images/implanter2 1.png';
    import SalonCoiffure from '$lib/images/u9lyuns3drewo1gj5p8m 1.png';
</script>

<div class="section-about">
    <h2>À PROPOS DE NOUS</h2>
    <p>Nous sommes 2 esthéticiennes indépendantes qui se sont lancés en janvier 2025, dans le but de répondre au mieux aux besoins de leurs clientèle. C’est pourquoi nous ferons toujours de notre mieux pour vous faire passer le meilleur moment.</p>
    <div class="estheticiennes">
        <div class="estheticienne-description">
            <h3>Anaïs</h3>
            <p>Étant diplômée du CAP, BP et BTS esthétique avec plus de 7 ans d’expérience dans
                le domaine, j’ai décidé d’ouvrir mon entreprise pour vous offrir des soins personnalisés avec
                des produits et méthodes respectueuses de votre peau. Je prends le temps de comprendre
                vos besoins pour vous garantir satisfaction et détente. Hâte de vous rencontrer pour
                partager ce moment beauté avec vous !</p>
            <button class="construction-btn"><b>Prendre rendez-vous 😄</b></button>
            <p class="description">Paiement au début de la scéance -
                (cartes ou espèces, pas de chèques) -
                Réservé uniquement aux femmes</p>
        </div>
        <div class="estheticienne-description">
            <h3>Alexandrine</h3>
            <p>Esthéticienne depuis plus de 2 ans, je suis passionnée par la beauté et le bien-être. Mon objectif est de vous offrir des soins personnalisés pour un moment de détente inoubliable. Que ce soit pour des épilations, des soins du visage ou des manucures, je mets tout en œuvre pour répondre à vos attentes. Hâte de vous accueillir et de partager ce moment de beauté avec vous !</p>
            <button class="construction-btn"><b>Prendre rendez-vous 😊</b></button>
            <p class="description">Paiement au début de la scéance -
            (cartes ou espèces, pas de chèques) -
            Réservé uniquement aux femmes</p>
        </div>
    </div>
    <p class="image-description">Après avoir écouté nos clients et c’est pourquoi au lieu de leur demander de se déplacer, nous nous déplacons directement à domicile afin de leur économiser le maximum de temps. Un entreprise à domicile basé à Oullins pour vous correspondre au mieux.</p>
    <img alt="Image du métro d'Oullins" src={OullinsMetro}/>
    <p class="image-description">Oullins nous semblait être le meilleur lieu de départ pour débuter notre activité, en cause de notre clientèle déjà bien établit et de la demande de celle-ci. Nous étions à l’origine esthéticiennes dans l’entreprise Yves Rocher mais après plusieurs années de travail, nous avons décidé de nous lancer à notre compte. Beaucoup de nos clientes nous on confier : préférer des prestations à domicile plutôt qu’en salon. Et nous avons décider de les écouter, c’est pourquoi aujourd’hui, nous proposons uniquement des prestations à domicile pour les femmes souhaitant prendre soin de leurs corps.</p>
    <img alt="Image de la mairie d'Oullins" src={OullinsMairie}/>
    <p class="image-description">Pour celles qui ne peuvent ou ne veulent pas avoir des prestations à domicile, nous avons prévu une petite surprise pour vous. Nous avons décider pour plaire au plus grand nombre de réserver un jour par semaine dans votre salon de coiffure à Oullins, en effet vous aurez la possibilité si vous ne pouvez pas ou ne préférez pas faire de prestation à domicile, de venir dans notre institut afin de vous faire chouchouter sur place.</p>
    <img alt="Image de notre salon de coiffure partenaire" src={SalonCoiffure}/>

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
        padding : 25px;
    }

    .section-about img{
        width : 800px;
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