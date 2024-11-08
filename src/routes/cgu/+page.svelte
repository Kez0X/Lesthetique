<svelte:head>
    <title>CGU - L'esthétique</title>
    <meta name="description" content="Découvrez nos services d'épilation réalisés avec des cires bio certifiées." />
</svelte:head>

<div class="section-about">
    <h1>Conditions Générales d’Utilisation</h1>

    <h2>1. Introduction</h2>
    <p>Les présentes Conditions Générales d’Utilisation (CGU) régissent l’accès et l’utilisation des services proposés par L’ESTHETIQUEAA, esthéticiennes à domicile, à nos clientes. En faisant appel à nos services, vous acceptez de respecter les conditions décrites ci-dessous.</p>

    <h2>2. Services</h2>
    <p>Nous proposons des services de soins esthétiques à domicile, comprenant, sans s’y limiter, les prestations suivantes :</p>
    <ul>
        <li>Soins du visage et du corps</li>
        <li>Manucure, pédicure et pose de vernis semi-permanent</li>
        <li>Épilation</li>
        <li>Réhaussement de cils</li>
    </ul>
    <p>Les détails des prestations, y compris les prix, peuvent être consultés sur notre site internet, ou nos flyers et peuvent être modifiés à tout moment.</p>

    <h2>3. Prise de rendez-vous</h2>
    <p>La prise de rendez-vous peut s’effectuer par téléphone, SMS et/ou via nos réseaux sociaux. La confirmation de votre rendez-vous sera communiquée par SMS uniquement. Nous nous réservons le droit de refuser un rendez-vous si les informations fournies sont incorrectes ou incomplètes.</p>
    <p>Toute annulation doit être faite au moins 24H avant le rendez-vous. Passé ce délai, nous nous réservons le droit de refuser la reprise de rendez-vous.</p>

    <h2>4. Obligations des clientes</h2>
    <p>En utilisant nos services, vous acceptez de :</p>
    <ul>
        <li>Fournir des informations exactes et complètes lors de la prise de rendez-vous</li>
        <li>Respecter les horaires convenus pour les rendez-vous</li>
        <li>Informer notre personnel de tout problème de santé, allergie ou condition particulière pouvant affecter la prestation du service</li>
    </ul>
    <p>En cas de comportement inapproprié, irrespectueux ou contraire à nos valeurs, nous nous réservons le droit d’annuler un rendez-vous ou de refuser de fournir nos services à l’avenir.</p>

    <h2>5. Prix et modalités de paiement</h2>
    <p>Les prix de nos prestations sont indiqués en euros et peuvent être modifiés à tout moment. Le prix applicable est celui en vigueur au moment de la réservation du service. Le paiement peut être effectué par espèces et carte bancaire au début de chaque rendez-vous.</p>

    <h2>6. Responsabilité</h2>
    <p>Nous mettons tout en œuvre pour fournir des services de qualité, adaptés aux besoins et attentes de chaque cliente. Cependant, nous déclinons toute responsabilité en cas de :</p>
    <ul>
        <li>Réactions allergiques ou problèmes de santé non signalés au préalable</li>
        <li>Dommages ou pertes causés par des produits que nous ne fournissons pas directement</li>
    </ul>
    <p>Notre responsabilité ne saurait être engagée pour des incidents ou événements imprévus, tels que des retards dus à des conditions de circulation ou à des événements imprévus.</p>

    <h2>7. Force majeure</h2>
    <p>Nous ne serons pas tenues responsables de tout manquement ou retard dans l’exécution de nos services en cas de force majeure, tels que des événements imprévus échappant à notre contrôle (catastrophes naturelles, grèves, pandémies, etc.).</p>

    <h2>8. Protection des données</h2>
    <p>Toutes les données personnelles que nous collectons dans le cadre de la prestation de nos services sont traitées conformément à notre Politique de Confidentialité, qui est disponible sur notre site internet.</p>

    <h2>9. Modification des CGU</h2>
    <p>Nous nous réservons le droit de modifier les présentes Conditions Générales d’Utilisation à tout moment. Les modifications prendront effet dès leur publication sur notre site internet ou dès leur communication par tout autre moyen. Il vous appartient de consulter régulièrement ces CGU pour prendre connaissance des éventuelles modifications.</p>

    <h2>10. Loi applicable et juridiction compétente</h2>
    <p>Les présentes CGU sont régies par la loi n° 94-665 du 4 août 1994. Tout litige relatif à l’exécution ou à l’interprétation des présentes CGU relèvera de la compétence des tribunaux français.</p>

    <h2>11. Contact</h2>
    <p>Pour toute question concernant ces CGU, vous pouvez nous contacter à :</p>
    <ul>
        <li>L’ESTHETIQUEAA</li>
        <li>Email : esthetiqueaa69@gmail.com</li>
        <li>Téléphone : 06 60 36 34 06</li>
    </ul>

    <p>Ces CGU sont un cadre légal pour vos services et doivent être adaptées à votre activité et à la réglementation locale. Si vous proposez des services en ligne, des conditions supplémentaires peuvent s’appliquer, comme celles relatives à la protection des données ou aux moyens de paiement en ligne.</p>
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