<script>
    import Brochure from '$lib/images/Beige Organic Beauty and Spa Brochure.pdf.pdf';
</script>

<div class="footer">
    <div class="footer-container">
        <div class="section-right">
            <h3>Nous contacter</h3>
            <ul>
                <li>Par mail : esthetiqueaa69@gmail.com</li>
                <li>Par instagram : estheticienne69</li>
                <li>Par facebook : anaïs delice</li>
            </ul>
            <h3>Nos CGU</h3>
            <a href="/cgu" >Nos conditions générales d'utilisation</a>
            <h3>Les moyens de paiements</h3>
            <ul>
                <li>Carte bleue</li>
                <li>Espèces</li>
            </ul>
        </div>
        <div class="section-left">
            <h3>Nos prestations</h3>
            <ul>
                <li>Onglerie : mains & pieds</li>
                <li>Epilation : tout le corps</li>
                <li>Massage : dos & jambes</li>
            </ul>
            <a href="{Brochure}">Télécharger la brochure complète</a>
            <h3>Notre politique</h3>
            <a href="/politique_de_confidentialite">Politique de confidentialité</a>
        </div>
    </div>
</div>

<style>
    .footer{
        background-color: #fbcfd1; /* Rose pastel */
        width: 100%;
        color: #333;
        margin-bottom : 0;
        margin-top : 10%;
        padding : 10px 70px;
    }

    .footer-container{
        display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Ajuste la largeur de chaque carte */
		max-width: 1400px; /* Limite la largeur totale de la grille */
		margin: 0 auto;
		gap: 20px;
		padding: 0 5%;
    }

    a{
    text-decoration: none;
		color: #333;
		font-weight: bold;
		font-size: 1em;
        text-decoration:underline;
    }

    .footer h3{
        font-size: 1.2em;
        color: #333;
        margin-bottom: 10px;
        margin-top : 30px;
        font-family: 'Dancing Script', cursive;
    }
    
</style>