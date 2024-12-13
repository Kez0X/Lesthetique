<script>
    import OullinsMetro from '$lib/images/8570_671_Inauguration-Oullins-St-Genis-Laval-51 1.png';
    import OullinsMairie from '$lib/images/implanter2 1.png';
    import SalonCoiffure from '$lib/images/u9lyuns3drewo1gj5p8m 1.png';
</script>

<div class="section-about">
    <h2>À PROPOS DE L'ESTHÉTIQUE AA</h2>
    <p>
        Bienvenue chez L'Esthétique AA, votre spécialiste de l'esthétique à domicile pour femmes à Oullins et ses environs. 
        Nous offrons des prestations de qualité adaptées à vos besoins, notamment des massages relaxants, des épilations, 
        et des soins ongulaires. Grâce à notre service mobile, nous nous déplaçons dans les communes d'Oullins, Saint-Genis-Laval, 
        Sainte-Foy-lès-Lyon, La Mulatière, Tassin, Millery, Charly, Vernaison, Irigny, Brignais, Chaponost et Pierre-Bénite, 
        pour recréer l’ambiance d’un institut de beauté directement chez vous.
    </p>
    <p>
        Notre mission est simple : offrir des moments de bien-être, dans un cadre de douceur et de professionnalisme. 
        Que ce soit pour une épilation parfaite, une manucure élégante ou un massage apaisant, nous veillons à ce que chaque prestation soit une expérience unique et personnalisée.
    </p>

    <div class="estheticiennes">
        <div class="estheticienne-description">
            <h3>Anaïs</h3>
            <p>
                Je suis Anaïs, diplômée du CAP, BP et BTS esthétique, avec plus de 7 ans d'expérience dans le domaine. 
                Mon objectif est de vous proposer des soins esthétiques respectueux de votre peau et de vos besoins, 
                en utilisant des produits professionnels de haute qualité. Que vous soyez à Oullins, Saint-Genis-Laval ou 
                Sainte-Foy-lès-Lyon, je suis à votre service pour vous offrir un moment de détente à domicile. 
                Hâte de partager ce moment beauté avec vous !
            </p>
            <button class="construction-btn" on:click={() => window.location.href = '/contact'}>
                <b>Prendre rendez-vous 😊</b>
            </button>
            <p class="description">
                Paiement au début de la séance - (cartes ou espèces, pas de chèques) - Réservé uniquement aux femmes.
            </p>
        </div>
        <div class="estheticienne-description">
            <h3>Alexandrine</h3>
            <p>
                Je suis Alexandrine, passionnée par la beauté et le bien-être depuis plus de 2 ans. 
                J’ai rejoint Anaïs pour créer L'Esthétique AA et offrir des soins personnalisés à nos clientes. 
                Que vous habitiez à La Mulatière, Tassin, ou Brignais, je mets tout en œuvre pour vous garantir un moment de détente, 
                qu'il s'agisse de soins des mains, d'épilations ou de massages. Prenons le temps ensemble de célébrer votre beauté !
            </p>
            <button class="construction-btn" on:click={() => window.location.href = '/contact'}>
                <b>Prendre rendez-vous 😊</b>
            </button>
            <p class="description">
                Paiement au début de la séance - (cartes ou espèces, pas de chèques) - Réservé uniquement aux femmes.
            </p>
        </div>
    </div>

    <div class="image-section">
        <div class="image-with-description">
            <img alt="Image du métro d'Oullins" src={OullinsMetro} />
            <p>
                Nous avons choisi d’offrir des prestations à domicile pour répondre aux besoins d’une clientèle souhaitant 
                gagner du temps et profiter d’un service flexible. Que vous soyez à Vernaison, Millery, ou Chaponost, 
                nous recréons l’ambiance relaxante et cocooning d’un institut de beauté, directement chez vous.
            </p>
        </div>

        <div class="image-with-description">
            <img alt="Image de la mairie d'Oullins" src={OullinsMairie} />
            <p>
                Oullins, berceau de notre aventure professionnelle, reste au cœur de nos prestations. 
                C’est un point central qui nous permet de rayonner dans les communes voisines, telles que Pierre-Bénite, 
                Irigny et Charly, pour offrir nos services esthétiques de qualité à une clientèle variée.
            </p>
        </div>

        <div class="image-with-description">
            <img alt="Image de notre salon de coiffure partenaire" src={SalonCoiffure} />
            <p>
                Pour certaines prestations spécifiques, comme les épilations du visage, les soins des mains et la pose de 
                vernis semi-permanent, retrouvez-nous au salon Line’s Coiffure, situé au 11 bis boulevard de l’Europe à Oullins. 
                Accessible en transport en commun, avec stationnement gratuit, ce lieu nous permet de vous accueillir dans un cadre chaleureux et pratique.
            </p>
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