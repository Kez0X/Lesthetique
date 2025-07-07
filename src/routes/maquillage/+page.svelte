<svelte:head>
    <title>Maquillage Professionnel à Domicile - L'esthétiqueAA</title>
    <meta name="description" content="Profitez de nos services de maquillage à domicile : maquillage de jour, maquillage de soirée, mariée, et plus. Disponible à Oullins, Saint-Genis-Laval, Sainte-Foy-lès-Lyon et les environs." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthetique AA, l'esthétique AA, L'Esthétique AA, Esthetique AA, esthetique AA Oullins, l'esthetiqueAA Oullins, L'EsthetiqueAA Oullins, Esthetique AA Oullins, esthetique à domicile, esthetique AA domicile, l'esthétique AA, esthétique AA, Esthétique AA, L'Esthetique AA, Esthétique AA">

        <script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],j=d.createElement(s);j.async=true;j.src="https://d.aa-esthetiqueoullins.fr/cop9gnmmemlp.js?"+i;f.parentNode.insertBefore(j,f);})(window,document,'script','dataLayer','k=aWQ9R1RNLVBSVjVDU0JX&sort=desc');</script>


</svelte:head>
<script>
    import OnglerieImage from '$lib/images/onglerie.png';

    let prestations = [
        { name: "Mariée", time: "-", price: "80€", description: "Une séance essaie & jour J" },
        { name: "Maquillage soirée", time: "45min", price: "40€", description: "-" }
    ];
</script>

    <noscript><iframe src="https://d.aa-esthetiqueoullins.fr/ns.html?id=GTM-PRV5CSBW" height="0" width="0" title="" style="display:none;visibility:hidden"></iframe></noscript>


<div class="onglerie-page">
    <!-- Image de fond et titre -->
    <div class="header-section" style="background-image: url({OnglerieImage});">
        <div class="overlay"></div>
        <h1>Prestations Maquillage</h1>
    </div>

    <!-- Tableau des prestations -->
    <div class="prestations-table">
        <table>
            <thead>
                <tr>
                    <th>Prestations</th>
                    <th>Temps</th>
                    <th>Prix</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                {#each prestations as prestation}
                    <tr>
                        <td>{prestation.name}</td>
                        <td>{prestation.time}</td>
                        <td>{prestation.price}</td>
                        <td>{prestation.description ? prestation.description : "-"}</td>
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <p>Le maquillage est réalisé avec des produits conventionnels.</p>
</div>

<style>
    .header-section {
        position: relative;
        height: 300px;
        background-size: cover;
        background-position: center;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
        text-align: center;
        font-family: Arial, sans-serif;
    }

    .header-section .overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.5);
        z-index: 1;
    }

    .header-section h1 {
        position: relative;
        z-index: 2;
        font-size: 2.5em;
        font-weight: bold;
        color: #ffe3e9;
    }

    .prestations-table {
        max-width: 800px;
        margin: 30px auto;
        padding: 20px;
        background: #fdf6f9;
        border-radius: 10px;
        box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
        font-family: Arial, sans-serif;
    }

    .prestations-table table {
        width: 100%;
        border-collapse: collapse;
    }

    .prestations-table th {
        padding: 12px 8px;
        background-color: #ffebf0;
        color: #d45a72;
        font-size: 1em;
        font-weight: bold;
        text-align: left;
        border-bottom: 2px solid #ffe3e9;
    }

    .prestations-table td {
        padding: 10px 8px;
        border-bottom: 1px solid #ffe3e9;
        color: #555;
    }

    p{
        text-align : center;
        font-size : 1em;
        margin-top : 20px;
        font-family: 'Crimson Text', sans-serif;
        font-weight : bold;
        color : #4A4A4A;
    }

    .prestations-table tbody tr:nth-child(odd) {
        background-color: #fff8fa;
    }

    .prestations-table td, .prestations-table th {
        padding: 12px;
    }

    @media (max-width: 768px) {
        .header-section h1 {
            font-size: 2em;
        }

        .prestations-table {
            padding: 15px;
        }

        .prestations-table th, .prestations-table td {
            padding: 8px;
            font-size: 0.9em;
        }
    }
</style>
