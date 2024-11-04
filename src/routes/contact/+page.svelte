<svelte:head>
	<title>L'esthétique - Contact</title>
	<meta name="description" content="" />
</svelte:head>


<script>
    import InstagramIcon from '$lib/images/Instagram.webp'; // Importez l'icône Instagram
    import FacebookIcon from '$lib/images/Facebook.png'; // Importez l'icône Facebook
</script>

<div class="contact-page">
    <h1>Contactez-nous pour prendre rendez-vous</h1>
    <p>Par Appel ou par SMS / Email / Facebook / Instagram (réponse sous 24h à 48h) :</p>
    <div class="contact-info">
        <p><strong>Anaïs :</strong> +33 0 00 00 00 00</p>
        <p><strong>Alexandrine :</strong> +33 0 00 00 00 00</p>
        <p>Contactez-nous par mail : <a href="mailto:lesthetiqueA&A@gmail.com">lesthetiqueA&A@gmail.com</a></p>
    </div>
    <div class="social-icons">
        <a href="#"><img src={FacebookIcon} alt="Facebook" /></a>
        <a href="https://www.instagram.com/anaisdelice.estheticienne69"><img src={InstagramIcon} alt="Instagram" /></a>
    </div>
    <p class="payment-info">Paiement au début de la séance. Réservé uniquement aux femmes.</p>

    <!-- Sections supplémentaires (par exemple FAQ) -->
    <div class="faq-section">
        <h2>Que dois-je dire lors de l'appel ?</h2>
        <p>Appelez nous, si vous avez un interlocuteur au bout du fil, parfait, dites lui les modalités de votre rendez-vous : à domicile ou en institut, votre nom, la date, l’heure, l’adresse (si nécéssaire), le nom de votre esthéticienne et la prestation. Sinon, vous pouvez laisser un message vocal avec toutes ses informations, et on vous rappelera pour confirmer la prise de rendez-vous.</p>
    </div>
    <div class="faq-section">
        <h2>Voir comment écrire le message</h2>
        <p>Envoyez nous un message ou un mail pour prendre rendez-vous à domicile, vous devez précisez qui vous êtes, à quelle heure souhaiteriez vous prendre rendez-vous,  quel jour et si votre rendez-vous est à domicile, votre adresse (notre politique de confidentialité garantit la sécurité de vos  données), votre esthéticienne et la prestation que vous souhaitez.</p>
    </div>
</div>

<style>
    .contact-page {
        text-align: center;
        background: #f8f8f8;
        padding: 20px;
        border-radius: 8px;
        max-width: 800px;
        margin: 0 auto;
    }
    .contact-info {
        margin-top: 20px;
        font-size: 1.1em;
    }
    .social-icons img {
        width: 40px;
        height: 40px;
        margin: 10px;
    }
    .payment-info {
        font-weight: bold;
        margin-top: 20px;
    }
    .faq-section {
        background: #ffebf0;
        padding: 15px;
        border-radius: 5px;
        margin-top: 15px;
        text-align: left;
    }
</style>
