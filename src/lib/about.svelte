<script>
    import AboutImage1 from '$lib/images/AboutImage1.jpg';
    import AboutImage2 from '$lib/images/AboutImage2.jpg';
    import AboutImage3 from '$lib/images/AboutImage3.jpg';
    import AboutImage4 from '$lib/images/AboutImage4.jpg';
    import AboutImage5 from '$lib/images/AboutImage5.jpg';
    import AboutImage6 from '$lib/images/AboutImage6.jpg';
    import AboutImage7 from '$lib/images/AboutImage7.jpg';
    import AboutImage8 from '$lib/images/AboutImage8.jpg';
    import AboutImage9 from '$lib/images/AboutImage9.jpg';
    import AboutImage10 from '$lib/images/AboutImage10.jpg';
    import AboutImage11 from '$lib/images/AboutImage11.jpg';
    import AboutImage12 from '$lib/images/AboutImage12.jpg';
    import AboutImage13 from '$lib/images/AboutImage13.jpg';

    // Images pour le fond
    import FlowerSummer from '$lib/images/FlowerSummer.svg';
    import FlowerWinter from '$lib/images/FlowerWinter.svg';
    import Petale1 from '$lib/images/Petale1.svg';
    import Petale2 from '$lib/images/Petale2.svg';
    import Petale3 from '$lib/images/Petale3.svg';
    import Petale4 from '$lib/images/Petale4.svg';
    import Petale5 from '$lib/images/Petale5.svg';
    import Petale6 from '$lib/images/Petale6.svg';

</script>

<div class="section-about">
  <!-- Images décoratives en fond -->
    <!-- Décorations florales SVG -->
    <img src={FlowerSummer} class="bg-deco deco1" alt="" aria-hidden="true" />
    <img src={FlowerWinter} class="bg-deco deco2" alt="" aria-hidden="true" />
    <img src={FlowerWinter} class="bg-deco deco9" alt="" aria-hidden="true" />
    <img src={FlowerSummer} class="bg-deco deco10" alt="" aria-hidden="true" />

    <!-- Pétales en pluie -->
    <img src={Petale1} class="bg-deco deco3" alt="" aria-hidden="true" />
    <img src={Petale2} class="bg-deco deco4" alt="" aria-hidden="true" />
    <img src={Petale3} class="bg-deco deco5" alt="" aria-hidden="true" />
    <img src={Petale4} class="bg-deco deco6" alt="" aria-hidden="true" />
    <img src={Petale5} class="bg-deco deco7" alt="" aria-hidden="true" />
    <img src={Petale6} class="bg-deco deco8" alt="" aria-hidden="true" />

    <!-- Petites duplications aléatoires pour créer un effet de pluie -->
    <img src={Petale1} class="bg-deco deco11" alt="" aria-hidden="true" />
    <img src={Petale2} class="bg-deco deco12" alt="" aria-hidden="true" />
    <img src={Petale3} class="bg-deco deco13" alt="" aria-hidden="true" />
    <img src={Petale4} class="bg-deco deco14" alt="" aria-hidden="true" />
    <img src={Petale5} class="bg-deco deco15" alt="" aria-hidden="true" />
    <img src={Petale6} class="bg-deco deco16" alt="" aria-hidden="true" />
    <img src={Petale2} class="bg-deco deco17" alt="" aria-hidden="true" />
    <img src={Petale3} class="bg-deco deco18" alt="" aria-hidden="true" />
    <img src={Petale5} class="bg-deco deco19" alt="" aria-hidden="true" />


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
          <img class="img1" src={AboutImage2} alt="Mairie Oullins" />
          <img class="img2" src={AboutImage6} alt="Oullins Ville" />
          <img class="img3" src={AboutImage10} alt="Grande rue d'oullins" />
        </div>
  
        <div class="album-text fade-slide-in">
          <p>
            Nous avons choisi d’offrir des prestations à domicile 🏠 pour répondre aux besoins d’une clientèle 
            souhaitant gagner du temps et profiter d’un service flexible. Que vous soyez à Vernaison, Millery, ou Chaponost, 
            nous recréons l’ambiance <b>relaxante</b> et <b>cocooning</b> d’un institut de beauté, directement chez vous.
            <br/>
            Nos prestations à domicile incluent notamment des soins du visage et du corps, une nouvelle beauté des mains et des pieds, des épilations, des massages bien-être et du maquillage pour événements
            <br/>
            Nous mettons un point d'honneur à vous offrir un moment de détente privilégié, dans le confort de votre foyer. Tout est pensé pour que vous puissiez vous offrir une pause beauté, sans contrainte de transport ni de stationnement.
          </p>
        </div>
      </div>
      <div class="image-album-section">  
        <div class="album-text fade-slide-in">
          <p>
            Pour certaines prestations spécifiques (épilations visage, soins des mains, vernis semi-permanent), 
            retrouvez-nous chez notre partenaire Line’s Coiffure 💅, au 11 bis boulevard de l’Europe à Oullins. 
            Facilement accessible en transport 🚇 avec stationnement gratuit, ce lieu chaleureux vous accueille avec plaisir.
          </p>

          <p>Ce partenariat nous permet de maintenir notre exigence de qualité tout en vous proposant un cadre accueillant et professionnel. C’est l’occasion de découvrir un salon convivial, facile d’accès, où vous serez reçue avec bienveillance et expertise.</p>
        </div>
        <div class="album-images">
          <img class="img1" src={AboutImage4} alt="Salon d'esthétique Oullins" />
          <img class="img2" src={AboutImage1} alt="Salon d'esthétique Oullins" />
          <img class="img3" src={AboutImage5} alt="Salon d'esthétique Oullins" />
        </div>
        
      </div>
      <div class="image-album-section">
        <div class="album-images">
          <img class="img1" src={AboutImage9} alt="Bouche de métro Oullins" />
          <img class="img2" src={AboutImage11} alt="Place Oullins" />
          <img class="img3" src={AboutImage12} alt="Métro Oullins" />
        </div>
        <div class="album-text fade-slide-in">
          <p>
            Oullins, berceau de notre aventure professionnelle 📍, reste au cœur de nos prestations. 
            C’est un point central qui nous permet de rayonner dans les communes voisines comme Pierre-Bénite, 
            Irigny et Charly pour offrir nos services esthétiques de qualité à une clientèle variée. Voici comment nous rejoindre :
          </p>
          <p>En transport en commun :<br/>Le métro B (station Oullins Centre) vous dépose à deux pas du salon Line’s Coiffure. Des bus desservent également les communes proches comme Saint-Genis-Laval, Pierre-Bénite ou La Mulatière.</p>
          <p>En voiture :<br/>Le salon dispose de places de stationnement gratuites à proximité, vous évitant les tracas habituels du centre-ville.</p>
          <p>À pied ou à vélo :<br/>Depuis le centre d’Oullins, l’accès est facile à pied, et des pistes cyclables facilitent également l’accès en deux roues.</p>
          <p>Oullins est un point stratégique qui permet à notre équipe d’être rapidement sur place pour vos soins à domicile, ou pour vous accueillir dans les meilleures conditions en salon.</p>
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
        position: relative;
        overflow: hidden;


    }

    .bg-deco {
      position: absolute;
      width: 60px; /* taille réduite */
      height: auto;
      opacity: 0.22; /* opacité légèrement augmentée */
      pointer-events: none;
      z-index: 0;
    }

    /* Fleurs principales */
    .deco1 { top: 40px; left: 5%; width: 100px; }
    .deco2 { top: 200px; right: 10%; width: 100px; }
    .deco9 { bottom: 80px; left: 15%; width: 80px; }
    .deco10 { top: 450px; right: 20%; width: 80px; }

    /* Pétales tombants - taille réduite et rotation douce */
    .deco3 { top: 120px; left: 10%; transform: rotate(25deg); }
    .deco4 { top: 250px; left: 35%; transform: rotate(-15deg); }
    .deco5 { top: 480px; right: 15%; transform: rotate(10deg); }
    .deco6 { bottom: 100px; right: 5%; transform: rotate(-30deg); }
    .deco7 { top: 400px; left: 20%; transform: rotate(12deg); }
    .deco8 { bottom: 220px; left: 40%; transform: rotate(-5deg); }

    /* Duplications supplémentaires */
    .deco12 { bottom: 250px; right: 10%; transform: rotate(-20deg); }
    .deco13 { top: 300px; left: 70%; transform: rotate(18deg); }
    .deco14 { top: 90px; right: 30%; transform: rotate(12deg); }
    .deco15 { bottom: 180px; left: 25%; transform: rotate(-10deg); }
    .deco16 { top: 550px; right: 20%; transform: rotate(22deg); }
    .deco17 { top: 180px; left: 45%; transform: rotate(-8deg); }
    .deco18 { bottom: 300px; right: 40%; transform: rotate(30deg); }
    .deco19 { top: 380px; left: 5%; transform: rotate(15deg); }



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
        border : 2px white solid;
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