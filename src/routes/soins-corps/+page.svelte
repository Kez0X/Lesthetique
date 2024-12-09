<svelte:head>
    <title>Soins du Corps Bio - Esthéticienne à Domicile - L'esthétiqueAA</title>
    <meta name="description" content="Découvrez nos soins du corps avec des huiles végétales bio pour une expérience de bien-être unique. Profitez de massages relaxants et revitalisants réalisés par nos esthéticiennes à domicile à Oullins, Saint-Genis-Laval, Sainte-Foy-lès-Lyon, et alentours." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthetiqueAA, l'esthetiqueAA, L'EsthetiqueAA, EsthetiqueAA, esthetiqueAA Oullins, l'esthetiqueAA Oullins, L'EsthetiqueAA Oullins, EsthetiqueAA Oullins, esthetique à domicile, esthetiqueAA domicile">
</svelte:head>


<script>
    import SoinsCorpsImage from '$lib/images/massages.png';

    let prestations = [
        { name: "Gommage", time: "30min", price: "35€" },
        { name: "Drainage lymphatique", time: "1h", price: "65€" },
        { name: "Drainage minceur", time: "1h", price: "75€" },
        { name: "Cure de 6 séances", time: "1h", price: "420€ - 70€/séance" },
        { name: "Relaxant", time: "30min", price: "35€" },
        { name: "Relaxant", time: "1h", price: "65€" },
        { name: "Forfait bien être 1h visage + 1h corps", time: "2h", price: "117€" },
        { name: "Forfait Spa 1h visage + 1h corps + gommage corps", time: "2h 30min", price: "148€" }
    ];
</script>

<div class="soins-corps-page">
    <div class="header-section" style="background-image: url({SoinsCorpsImage})">
        <div class="overlay"></div>
        <h1>Prestations Soins du Corps</h1>
    </div>

    <div class="prestations-table">
        <table>
            <thead>
                <tr>
                    <th>Prestations</th>
                    <th>Temps</th>
                    <th>Prix</th>
                </tr>
            </thead>
            <tbody>
                {#each prestations as prestation}
                    <tr>
                        <td>{prestation.name}</td>
                        <td>{prestation.time}</td>
                        <td>{prestation.price}</td>
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <p>Les soins du corps sont réalisés avec des huiles végétales. 🍃</p>
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

    .prestations-table tbody tr:nth-child(odd) {
        background-color: #fff8fa;
    }

    .prestations-table td, .prestations-table th {
        padding: 12px;
    }

    p{
        text-align : center;
        font-size : 1em;
        margin-top : 20px;
        font-family: 'Crimson Text', sans-serif;
        font-weight : bold;
        color : #4A4A4A;
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
