<svelte:head>
    <title>Contact - L'EsthetiqueAA</title>
    <meta name="description" content="Contactez L'esthétique pour prendre rendez-vous et découvrir nos prestations." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthétique AA, l'esthétique AA, Esthetique AA, esthetique AA Oullins, esthetique à domicile">
</svelte:head>

<script>
    import InstagramIcon from '$lib/images/Instagram.webp';
    import FacebookIcon from '$lib/images/Facebook.png';

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

<div class="contact-wrapper">
    <!-- Décoration florale -->
    <img src={FlowerSummer} class="bg-deco deco1" alt="" aria-hidden="true" />
    <img src={FlowerWinter} class="bg-deco deco2" alt="" aria-hidden="true" />
    <img src={Petale1} class="bg-deco deco3" alt="" aria-hidden="true" />
    <img src={Petale2} class="bg-deco deco4" alt="" aria-hidden="true" />
    <img src={Petale3} class="bg-deco deco5" alt="" aria-hidden="true" />
    <img src={Petale4} class="bg-deco deco6" alt="" aria-hidden="true" />
    <img src={Petale5} class="bg-deco deco7" alt="" aria-hidden="true" />
    <img src={Petale6} class="bg-deco deco8" alt="" aria-hidden="true" />

    <div class="contact-page">
        <h1>Contactez-nous</h1>
        <p>Joignez-nous par appel, SMS ou via les réseaux sociaux.</p>

        <div class="contact-info">
            <p><strong>Anaïs :</strong> <a href="tel:+33660363406">+33 6 60 36 34 06</a></p>
            <p><strong>Alexandrine :</strong> <a href="tel:+33624748716">+33 6 24 74 87 16</a></p>
        </div>

        <a class="btn-planity" href="https://www.treatwell.fr/salon/l-esthetique-aa-estheticiennes-a-domicile/" target="_blank" rel="noopener noreferrer">
            Réserver via Treatwell
        </a>

        <div class="social-icons">
            <a href="https://www.facebook.com/profile.php?id=61563897359229" aria-label="Facebook"><img src={FacebookIcon} alt="Facebook" /></a>
            <a href="https://www.instagram.com/lesthetiqueaa.69" aria-label="Instagram"><img src={InstagramIcon} alt="Instagram" /></a>
        </div>

        <p class="payment-info">💳 Paiement au début de la séance. Réservé uniquement aux femmes.</p>

        <div class="faq-section">
            <h2>Que dire lors de l'appel ?</h2>
            <p>Précisez si vous souhaitez un rendez-vous à domicile ou en institut, ainsi que vos coordonnées, la date et la prestation. Laissez un message vocal si besoin, nous vous rappellerons.</p>
        </div>

        <div class="faq-section">
            <h2>Par message ?</h2>
            <p>Envoyez votre nom, créneau souhaité, adresse (si à domicile), esthéticienne et prestation. Toutes vos données sont confidentielles.</p>
        </div>
    </div>
</div>


<style>
    /* Page générale */
    .contact-page {
        margin-top: 30px;
        background: linear-gradient(to bottom, #fff8fa, #ffffff);
        padding: 40px 20px;
        border-radius: 16px;
        max-width: 800px;
        margin: 30px auto;
        font-family: "Poppins", sans-serif;
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        text-align: center;
        line-height: 1.6;
    }

    /* Titre principal */
    h1 {
        font-size: 2em;
        color: #d45a72;
        margin-bottom: 20px;
        font-weight: bold;
    }

    /* Paragraphes généraux */
    p {
        color: #444;
        font-size: 1.1em;
        margin-bottom: 15px;
    }

    /* Section des informations de contact */
    .contact-info {
        background-color: #ffe3e9;
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        margin: 20px 0;
    }

    .contact-info p {
        font-weight: 500;
        margin: 8px 0;
    }

    .contact-info a {
        color: #d45a72;
        text-decoration: none;
        font-weight: bold;
    }

    .contact-info a:hover {
        text-decoration: underline;
    }

    /* Bouton Planity */
    .btn-planity {
        display: inline-block;
        margin: 20px 0;
        padding: 12px 20px;
        background-color: #ff7f7f;
        color: white;
        font-weight: bold;
        font-size: 1em;
        text-decoration: none;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        transition: background-color 0.3s ease, transform 0.3s ease;
    }

    .btn-planity:hover {
        background-color: #fb6f6f;
        transform: scale(1.05);
    }

    /* Réseaux sociaux */
    .social-icons {
        margin-top: 20px;
    }

    .social-icons a {
        display: inline-block;
        margin: 0 10px;
        transition: opacity 0.3s ease;
    }

    .social-icons a:hover {
        opacity: 0.8;
    }

    .social-icons img {
        width: 40px;
        height: 40px;
    }

    /* Informations de paiement */
    .payment-info {
        color: #d45a72;
        font-weight: bold;
        margin-top: 20px;
        font-size: 1em;
    }

    /* Section FAQ */
    .faq-section {
        background: #f9f9f9;
        padding: 20px;
        border-radius: 12px;
        margin-top: 25px;
        text-align: left;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
    }

    .faq-section h2 {
        font-size: 1.4em;
        color: #d45a72;
        font-weight: bold;
        margin-bottom: 10px;
    }

    .faq-section p {
        color: #555;
        font-size: 1em;
        line-height: 1.6;
        margin-bottom: 0;
    }

    /* Responsive design */
    @media (max-width: 768px) {
        .contact-page {
            padding: 20px;
        }

        h1 {
            font-size: 1.8em;
        }

        .faq-section h2 {
            font-size: 1.3em;
        }

        .social-icons img {
            width: 35px;
            height: 35px;
        }

        .btn-planity {
            padding: 10px 18px;
            font-size: 0.9em;
        }
    }


    .bg-deco {
        position: absolute;
        width: 60px;
        opacity: 0.12;
        z-index: 0;
        pointer-events: none;
    }

    /* Exemple de placements */
    .deco1 { top: 50px; left: 5%; width: 100px; }
    .deco2 { top: 200px; right: 5%; width: 80px; }
    .deco3 { top: 100px; left: 20%; transform: rotate(20deg); }
    .deco4 { top: 300px; right: 10%; transform: rotate(-10deg); }
    .deco5 { bottom: 100px; left: 10%; transform: rotate(15deg); }
    .deco6 { top: 400px; left: 30%; transform: rotate(-5deg); }
    .deco7 { bottom: 200px; right: 15%; transform: rotate(12deg); }
    .deco8 { top: 600px; left: 50%; transform: rotate(-18deg); }
</style>
