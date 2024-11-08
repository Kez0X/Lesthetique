<svelte:head>
    <title>L'esthétique - Contact</title>
    <meta name="description" content="Contactez L'esthétique pour prendre rendez-vous et découvrir nos prestations." />
</svelte:head>

<script>
    import InstagramIcon from '$lib/images/Instagram.webp';
    import FacebookIcon from '$lib/images/Facebook.png';
</script>

<div class="contact-page">
    <h1>Contactez-nous pour prendre rendez-vous</h1>
    <p>Par appel, SMS, Facebook ou Instagram (réponse sous 24h à 48h) :</p>

    <div class="contact-info">
        <p><strong>Anaïs :</strong> +33 6 60 36 34 06</p>
        <p><strong>Alexandrine :</strong> +33 0 00 00 00 00</p>
    </div>

    <div class="social-icons">
        <a href="https://www.facebook.com/profile.php?id=61563897359229"><img src={FacebookIcon} alt="Facebook" /></a>
        <a href="https://www.instagram.com/anaisdelice.estheticienne69"><img src={InstagramIcon} alt="Instagram" /></a>
    </div>

    <p class="payment-info">Paiement au début de la séance. Réservé uniquement aux femmes.</p>

    <!-- Section FAQ avec des exemples de questions -->
    <div class="faq-section">
        <h2>Que dois-je dire lors de l'appel ?</h2>
        <p>Appelez-nous et indiquez les détails de votre rendez-vous : à domicile ou en institut, votre nom, la date, l’heure, l’adresse (si nécessaire), le nom de votre esthéticienne et la prestation souhaitée. Si vous laissez un message vocal, mentionnez ces informations, et nous vous rappellerons pour confirmer.</p>
    </div>
    <div class="faq-section">
        <h2>Voir comment écrire le message</h2>
        <p>Envoyez un message ou un mail pour prendre rendez-vous. Précisez votre nom, l’heure et le jour souhaités, l’adresse si c'est à domicile, l’esthéticienne et la prestation choisie. Vos données sont sécurisées grâce à notre politique de confidentialité.</p>
    </div>
</div>

<style>
    /* Styles globaux pour la page de contact */
    .contact-page {
        background: linear-gradient(to bottom, #ffebf0, #f8f8f8);
        padding: 40px;
        border-radius: 12px;
        max-width: 700px;
        margin: 0 auto;
        font-family: Arial, sans-serif;
        box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
        text-align: center;
    }

    /* Style pour le titre de la page */
    h1 {
        font-size: 2em;
        color: #d45a72;
        margin-bottom: 20px;
        font-weight: bold;
    }

    /* Style pour les paragraphes */
    p {
        color: #555;
        font-size: 1.1em;
        margin-bottom: 15px;
    }

    /* Informations de contact */
    .contact-info {
        background-color: #ffe3e9;
        padding: 20px;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        margin-bottom: 20px;
    }

    .contact-info p {
        margin: 10px 0;
        font-weight: 500;
        color: #333;
    }

    .contact-info a {
        color: #d45a72;
        text-decoration: none;
        font-weight: bold;
    }

    .contact-info a:hover {
        text-decoration: underline;
    }

    /* Icônes des réseaux sociaux */
    .social-icons {
        margin-top: 20px;
    }

    .social-icons a {
        display: inline-block;
        margin: 0 10px;
        transition: transform 0.3s ease;
    }

    .social-icons a:hover {
        transform: scale(1.1);
    }

    .social-icons img {
        width: 35px;
        height: 35px;
    }

    /* Informations de paiement */
    .payment-info {
        color: #d45a72;
        font-weight: bold;
        margin-top: 20px;
        font-size: 1em;
    }

    /* Style de la FAQ */
    .faq-section {
        background: #ffe3e9;
        padding: 20px;
        border-radius: 8px;
        margin-top: 20px;
        text-align: left;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
    }

    .faq-section h2 {
        font-size: 1.3em;
        color: #d45a72;
        font-weight: bold;
        margin-bottom: 10px;
    }

    .faq-section p {
        color: #555;
        font-size: 1em;
        line-height: 1.6;
    }

    /* Responsive design */
    @media (max-width: 768px) {
        .contact-page {
            padding: 20px;
        }

        .social-icons img {
            width: 30px;
            height: 30px;
        }

        .contact-info, .faq-section {
            padding: 15px;
        }
    }
</style>
