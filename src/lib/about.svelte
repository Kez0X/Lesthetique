<script>
    import OullinsMetro from '$lib/images/8570_671_Inauguration-Oullins-St-Genis-Laval-51 1.png';
    import OullinsMairie from '$lib/images/implanter2 1.png';
    import SalonCoiffure from '$lib/images/u9lyuns3drewo1gj5p8m 1.png';
</script>

<div class="section-about">
    <div class="content">
      <h2>À PROPOS DE L'ESTHÉTIQUE AA 💖</h2>
      <p>
        Bienvenue chez L'Esthétique AA, votre spécialiste de l'esthétique à domicile pour femmes à Oullins et ses environs. 
        Nous offrons des prestations de qualité adaptées à vos besoins : massages relaxants, épilations, 
        et soins ongulaires. Grâce à notre service mobile 🚗, nous nous déplaçons dans les communes d'Oullins, 
        Saint-Genis-Laval, Sainte-Foy-lès-Lyon, La Mulatière, Tassin, Millery, Charly, Vernaison, Irigny, Brignais, 
        Chaponost et Pierre-Bénite pour recréer l’ambiance d’un institut de beauté directement chez vous.
      </p>
      <p>
        Notre mission est simple : offrir des moments de bien-être, dans un cadre de douceur et de professionnalisme. 
        Que ce soit pour une épilation parfaite, une manucure élégante ou un massage apaisant, chaque prestation est une expérience unique et personnalisée ✨.
      </p>
  
      <div class="estheticiennes">
        <div class="estheticienne-description">
          <h3>Anaïs</h3>
          <p>
            Je suis Anaïs, diplômée du CAP, BP et BTS esthétique, avec plus de 7 ans d'expérience dans le domaine. 
            Mon objectif est de vous proposer des soins esthétiques respectueux de votre peau, 
            en utilisant des produits professionnels de haute qualité. Que vous soyez à Oullins, Saint-Genis-Laval ou 
            Sainte-Foy-lès-Lyon, je suis à votre service pour vous offrir un moment de détente à domicile. 
            Hâte de partager ce moment beauté avec vous ! 🌸
          </p>
          <button class="construction-btn" on:click={() => window.location.href = '/contact'}>
            <b>Prendre rendez-vous 😊</b>
          </button>
          <p class="description">
            Paiement au début de la séance – (cartes ou espèces, pas de chèques)  
            <br>Réservé uniquement aux femmes.
          </p>
        </div>
  
        <div class="estheticienne-description">
          <h3>Alexandrine</h3>
          <p>
            Je suis Alexandrine, passionnée par la beauté et le bien-être depuis plus de 2 ans. 
            J’ai rejoint Anaïs pour créer L'Esthétique AA et offrir des soins personnalisés à nos clientes. 
            Que vous habitiez à La Mulatière, Tassin ou Brignais, je mets tout en œuvre pour vous garantir un moment de détente, 
            qu'il s'agisse de soins des mains, d'épilations ou de massages. Prenons le temps ensemble de célébrer votre beauté ! ✨
          </p>
          <button class="construction-btn" on:click={() => window.location.href = '/contact'}>
            <b>Prendre rendez-vous 😊</b>
          </button>
          <p class="description">
            Paiement au début de la séance – (cartes ou espèces, pas de chèques)  
            <br>Réservé uniquement aux femmes.
          </p>
        </div>
      </div>
  
      <div class="image-album-section">
        <div class="album-images">
          <img class="img1" src={OullinsMetro} alt="Métro Oullins" />
          <img class="img2" src={OullinsMairie} alt="Mairie Oullins" />
          <img class="img3" src={SalonCoiffure} alt="Salon partenaire" />
        </div>
  
        <div class="album-text fade-slide-in">
          <p>
            Nous avons choisi d’offrir des prestations à domicile 🏠 pour répondre aux besoins d’une clientèle 
            souhaitant gagner du temps et profiter d’un service flexible. Que vous soyez à Vernaison, Millery, ou Chaponost, 
            nous recréons l’ambiance relaxante et cocooning d’un institut de beauté, directement chez vous.
          </p>
  
          <p>
            Oullins, berceau de notre aventure professionnelle 📍, reste au cœur de nos prestations. 
            C’est un point central qui nous permet de rayonner dans les communes voisines comme Pierre-Bénite, 
            Irigny et Charly pour offrir nos services esthétiques de qualité à une clientèle variée.
          </p>
  
          <p>
            Pour certaines prestations spécifiques (épilations visage, soins des mains, vernis semi-permanent), 
            retrouvez-nous chez notre partenaire Line’s Coiffure 💅, au 11 bis boulevard de l’Europe à Oullins. 
            Facilement accessible en transport 🚇 avec stationnement gratuit, ce lieu chaleureux vous accueille avec plaisir.
          </p>
        </div>
      </div>
    </div>
  </div>

<style>
    /* Styles pour la section globale */
    .section-about {
        align-items: center;
        text-align : center;
        display : flex;
        width: 100%;
        text-align: center;
        padding: 50px 20px; /* Ajout de padding latéral */
        background-color: #ffffff;
    }

    .section-about .content{
        max-width : 1400px;
        margin : auto;
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

    .image-album-section {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 50px;
        flex-wrap: wrap;
        padding: 60px 20px;
        }

        .album-images {
        position: relative;
        width: 300px;
        height: 300px;
        }

        .album-images img {
        position: absolute;
        width: 200px;
        height: 200px;
        object-fit: cover;
        border-radius: 0px;
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        transition: transform 0.4s ease;
        cursor: pointer;
        }

        /* Image 1 */
        .album-images .img1 {
        top: 0;
        left: 0;
        z-index: 3;
        transform: rotate(-5deg);
        }

        /* Image 2 */
        .album-images .img2 {
        top: 20px;
        left: 40px;
        z-index: 2;
        transform: rotate(3deg);
        }

        /* Image 3 */
        .album-images .img3 {
        top: 40px;
        left: 80px;
        z-index: 1;
        transform: rotate(-2deg);
        }

        /* Hover effect to slightly move images */
        .album-images img:hover {
        transform: scale(1.05) rotate(0deg);
        z-index: 4;
        }

        .album-text {
        max-width: 600px;
        font-size: 1.05em;
        line-height: 1.7;
        color: #555;
        }

        /* Animation */
        .fade-slide-in {
        opacity: 0;
        transform: translateY(30px);
        animation: fadeSlideIn 1s ease forwards;
        animation-delay: 0.3s;
        }

        @keyframes fadeSlideIn {
        to {
            opacity: 1;
            transform: translateY(0);
        }
        }

        /* Responsive */
        @media (max-width: 768px) {
        .image-album-section {
            flex-direction: column;
            text-align: center;
        }

        .album-images {
            margin-bottom: 30px;
        }
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