<svelte:head>
    <title>Contact - L'EsthetiqueAA</title>
    <meta name="description" content="Contactez L'esthétique pour prendre rendez-vous et découvrir nos prestations." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthetique AA, l'esthétique AA, L'Esthétique AA, Esthetique AA, esthetique AA Oullins, l'esthetiqueAA Oullins, L'EsthetiqueAA Oullins, Esthetique AA Oullins, esthetique à domicile, esthetique AA domicile, l'esthétique AA, esthétique AA, Esthétique AA, L'Esthetique AA, Esthétique AA">
</svelte:head>

<script>
    import InstagramIcon from '$lib/images/Instagram.webp';
    import FacebookIcon from '$lib/images/Facebook.png';
</script>

<div class="contact-page">
    <h1>Contactez-nous</h1>
    <p>Joignez-nous par appel, SMS, Facebook ou Instagram. Réponse sous 24h à 48h.</p>

    <div class="contact-info">
        <p><strong>Anaïs :</strong> <a href="tel:+33660363406">+33 6 60 36 34 06</a></p>
        <p><strong>Alexandrine :</strong> <a href="tel:+33000000000">+33 6 24 74 87 16</a></p>
    </div>

    <div class="social-icons">
        <a href="https://www.facebook.com/profile.php?id=61563897359229" aria-label="Visitez notre page Facebook">
            <img src={FacebookIcon} alt="Facebook"/>
        </a>
        <a href="https://www.instagram.com/anaisdelice.estheticienne69" aria-label="Visitez notre page Instagram">
            <img src={InstagramIcon} alt="Instagram" />
        </a>
    </div>

    <p class="payment-info">💳 Paiement au début de la séance. Réservé uniquement aux femmes.</p>

    <a href="https://www.planity.com" target="_blank" class="btn-planity">
        Prendre rendez-vous sur Planity
    </a>

    <div class="faq-section">
        <h2>Que dire lors de l'appel ?</h2>
        <p>Appelez-nous et précisez si vous préférez un rendez-vous à domicile ou en institut. Indiquez votre nom, la date, l’heure, l’adresse (si nécessaire), le nom de l’esthéticienne et la prestation souhaitée. Si vous laissez un message vocal, mentionnez ces informations, et nous vous rappellerons pour confirmer.</p>
    </div>

    <div class="faq-section">
        <h2>Comment écrire un message ?</h2>
        <p>Envoyez-nous un message ou un e-mail pour réserver. Mentionnez votre nom, l’heure et le jour souhaités, l’adresse si c'est à domicile, l’esthéticienne et la prestation choisie. Vos données sont sécurisées grâce à notre politique de confidentialité.</p>
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
</style>
