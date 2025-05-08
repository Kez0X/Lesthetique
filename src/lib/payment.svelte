<div class="section-payment">
    <h2>LE REGLEMENT 💳</h2>
    <div class="payment-option">
        <h3><i class="fas fa-credit-card"></i> Carte Bleue</h3>
        <p>Nous disposons d’un TPE pour chacun des rendez-vous effectués avec les clients.</p>
    </div>
    <div class="payment-option">
        <h3><i class="fas fa-money-bill-wave"></i> Espèces</h3>
        <p>Nous acceptons aussi les espèces, sous réserve de vérification de la validité de celles-ci.</p>
    </div>
    <div class="payment-option">
        <h3><i class="fas fa-clock"></i> En Début de Séance</h3>
        <p>Les paiements seront effectués en début de séance pour nous protéger de toute tentative d’arnaque ou de fraude.</p>
    </div>
    <div class="payment-policy">
        <h3><i class="fas fa-undo-alt"></i> Notre Politique de Remboursement</h3>
        <p>Aucun remboursement ne sera effectué. Nous nous engageons à vous fournir la meilleure prestation possible. Cependant, si vous jugez que la prestation n’était pas à la hauteur de vos attentes, nous vous invitons à nous faire part de remarques constructives pour nous améliorer.</p>
    </div>
</div>

<!-- Inclure Font Awesome pour les icônes -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">


<style>
    /* Styles pour la section globale */
.section-payment {
    width: 100%;
    max-width: 1400px;
    margin: 0 auto;
    padding: 50px 20px;
}

.section-payment h2 {
    text-align: center;
    font-size: 2em;
    font-weight: bold;
    margin-bottom: 30px;
    color: #333;
}

.payment-option, .payment-policy {
    margin-bottom: 30px;
    padding: 20px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.payment-option:hover, .payment-policy:hover {
    transform: translateY(-5px);
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
}

.payment-option h3, .payment-policy h3 {
    font-size: 1.8em;
    font-weight: bold;
    color: #ff7f7f;
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 10px;
}

.payment-option p, .payment-policy p {
    font-size: 1em;
    line-height: 1.6;
    color: #555;
    margin: 0;
}

.payment-option i, .payment-policy i {
    font-size: 1.2em;
    color: #ff7f7f;
}

/* Effet de séparation entre les sections */
.payment-option:not(:last-child) {
    border-bottom: 1px solid #ddd;
}

/* Responsive design */
@media (max-width: 768px) {
    .section-payment {
        padding: 30px 15px;
    }

    .section-payment h2 {
        font-size: 2em;
    }

    .payment-option h3, .payment-policy h3 {
        font-size: 1.5em;
    }

    .payment-option p, .payment-policy p {
        font-size: 0.95em;
    }
}

</style>