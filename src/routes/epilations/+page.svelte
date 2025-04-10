<svelte:head>
    <title>Forfaits de Soins Visage et Corps - L'esthétiqueAA</title>
    <meta name="description" content="Découvrez nos forfaits personnalisés pour des soins du visage et du corps à domicile. Offrez-vous des moments de bien-être à Oullins, Saint-Genis-Laval et les environs." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthetique AA, l'esthétique AA, L'Esthétique AA, Esthetique AA, esthetique AA Oullins, l'esthetiqueAA Oullins, L'EsthetiqueAA Oullins, Esthetique AA Oullins, esthetique à domicile, esthetique AA domicile, l'esthétique AA, esthétique AA, Esthétique AA, L'Esthetique AA, Esthétique AA">
</svelte:head>
<script>
    import EpilationsImage from '$lib/images/epilations.png';

    let prestations_visage = [
        { name: "Sourcils", time: "15 min", price: "14€"},
        { name: "Lèvres", time: "10 min", price: "10€" },
        { name: "Menton", time: "10 min", price: "10€" },
        { name: "Joues", time: "15 min", price: "14€" },
        { name: "Forfaits visage complet", time: "45 min", price: "45€" },
        { name: "Forfaits sourcils + lèvres", time: "25 min", price: "22€" },
        { name: "Teinture", time: "5/10 min", price: "5€" }
        
    ];

    let prestations_corps = [
        { name: "1/2 jambes", time: "20 min", price: "20€"},
        { name: "Cuisses", time: "20 min", price: "20€"},
        { name: "Jambes complètes", time: "30 min", price: "28€"},
        { name: "Bras", time: "20 min", price: "28€"},
        { name: "1/2 bras", time: "15 min", price: "16€"},
        { name: "Maillot échancré", time: "20 min", price: "20€"},
        { name: "Maillot brésilien", time: "25 min", price: "26€"},
        { name: "Maillot complet", time: "30 min", price: "28€"},
        { name: "Aisselles", time: "15 min", price: "14€"},
        { name: "Bande supplémentaire", time: "10 min", price: "10€"}
    ];

    let forfaits_corps = [
        { name: "1/2 jambes, échancré, aisselles", time: "55 min", price: "50€"},
        { name: "1/2 jambes, complet, aisselles", time: "1 h 05 min", price: "59€"},
        { name: "Jambes complètes, échancré, aisselles", time: "1 h 15 min", price: "59€"},
        { name: "Jambes complètes, complet, aisselles", time: "1 h 15 min", price: "67€"}
    ];
</script>

<div class="epilations-page">
    <div class="header-section" style="background-image: url({EpilationsImage})">
        <div class="overlay"></div>
        <h1>Prestations Épilations</h1>
    </div>
    <h3>Epilations visages</h3>
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
                {#each prestations_visage as prestation}
                    <tr>
                        <td>{prestation.name}</td>
                        <td>{prestation.time}</td>
                        <td>{prestation.price}</td>
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <h3>Epilations corps</h3>
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
                {#each prestations_corps as prestation}
                    <tr>
                        <td>{prestation.name}</td>
                        <td>{prestation.time}</td>
                        <td>{prestation.price}</td>
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <h3>Forfaits corps</h3>
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
                {#each forfaits_corps as prestation}
                    <tr>
                        <td>{prestation.name}</td>
                        <td>{prestation.time}</td>
                        <td>{prestation.price}</td>
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <p>Les épilations sont réalisées avec des cires certifiées bio. 🍃</p>
    <p>les épilations visage sans autres prestations se feront directement au sein du salon Line’s coiffure situé au 11 bis boulevard de l’europe , 69600 oullins.</p>
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

    h3{
        text-align : center;
        font-size : 1.5em;
        margin-top : 30px;
        font-family: 'Crimson Text', sans-serif;
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
