<script>
    import Brochure from '$lib/images/Beige Organic Beauty and Spa Brochure.pdf.pdf';
</script>

<footer class="footer">
    <div class="footer-container">
        <div class="footer-column">
            <h3>Contact</h3>
            <ul>
                <li>
                    <a href="mailto:esthetiqueaa69@gmail.com">
                        <svg class="icon" viewBox="0 0 24 24" fill="none">
                            <path d="M4 4h16v16H4V4zm0 0l8 6 8-6" stroke="currentColor" stroke-width="1.5" />
                        </svg>
                        esthetiqueaa69@gmail.com
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/estheticienne69" target="_blank">
                        <svg class="icon" viewBox="0 0 24 24" fill="none">
                            <path d="M7 2h10a5 5 0 0 1 5 5v10a5 5 0 0 1-5 5H7a5 5 0 0 1-5-5V7a5 5 0 0 1 5-5zm5 5a5 5 0 1 0 0 10 5 5 0 0 0 0-10zm6.5-1a1 1 0 1 1-2 0 1 1 0 0 1 2 0z" stroke="currentColor" stroke-width="1.5"/>
                        </svg>
                        @estheticienne69
                    </a>
                </li>
                <li>
                    <a href="https://www.facebook.com/anaisdelice" target="_blank">
                        <svg class="icon" viewBox="0 0 24 24" fill="none">
                            <path d="M15 3h4v4h-4v4h4v4h-4v6h-4v-6H9v-4h2V7a4 4 0 0 1 4-4z" stroke="currentColor" stroke-width="1.5" />
                        </svg>
                        Anaïs Délice
                    </a>
                </li>
            </ul>
        </div>

        <div class="footer-column">
            <h3>Informations</h3>
            <ul>
                <li><a href="/cgu">Conditions générales</a></li>
                <li><a href="/politique_de_confidentialite">Politique de confidentialité</a></li>
                <li><a href="{Brochure}" download>Télécharger la brochure</a></li>
            </ul>
        </div>

        <div class="footer-column">
            <h3>Prestations</h3>
            <ul>
                <li>Onglerie : mains & pieds</li>
                <li>Épilation : tout le corps</li>
                <li>Massage : dos & jambes</li>
            </ul>
        </div>

        <div class="footer-column">
            <h3>Paiements</h3>
            <ul>
                <li>Carte bleue</li>
                <li>Espèces</li>
            </ul>
        </div>
    </div>
</footer>

<style>
    .footer {
        margin-top: 200px;
        background-color: #fff;
        color: #111;
        padding: 60px 40px;
        font-family: 'Inter', sans-serif;
        border-top: 1px solid #e5e5e5;
    }

    .footer-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 40px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .footer-column h3 {
        font-size: 1rem;
        font-weight: 600;
        margin-bottom: 1rem;
        text-transform: uppercase;
        letter-spacing: 0.05em;
    }

    .footer-column ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .footer-column li {
        margin-bottom: 0.6rem;
        font-size: 0.95rem;
        line-height: 1.4;
    }

    .footer a {
        display: flex;
        align-items: center;
        gap: 8px;
        text-decoration: none;
        color: #111;
        transition: opacity 0.2s ease;
        font-size: 0.95rem;
    }

    .footer a:hover {
        opacity: 0.6;
    }

    .icon {
        width: 18px;
        height: 18px;
        stroke: currentColor;
    }

    @media (max-width: 600px) {
        .footer {
            padding: 40px 20px;
        }

        .footer-column h3 {
            font-size: 0.95rem;
        }
    }
</style>
