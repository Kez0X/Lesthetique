<svelte:head>
    <title>Forfaits - L'esthétiqueAA</title>
    <meta name="description" content="Découvrez nos forfaits personnalisés pour des soins du visage et du corps à domicile. Offrez-vous des moments de bien-être à Oullins, Saint-Genis-Laval et les environs." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthetique AA, l'esthétique AA, L'Esthétique AA, Esthetique AA, esthetique AA Oullins, l'esthetiqueAA Oullins, L'EsthetiqueAA Oullins, Esthetique AA Oullins, esthetique à domicile, esthetique AA domicile, l'esthétique AA, esthétique AA, Esthétique AA, L'Esthetique AA, Esthétique AA">
</svelte:head>

<script>
    import ForfaitsImage from '$lib/images/forfaits.png';

    let prestations = [
        { name: "Forfaits visage complet épilation", time: "45 min", price: "45€" },
        { name: "Forfaits sourcils + lèvres épilation", time: "25 min", price: "22€" },
        { name: "1/2 jambes, échancré, aisselles", time: "55 min", price: "50€"},
        { name: "1/2 jambes, complet, aisselles", time: "1 h 05 min", price: "59€"},
        { name: "Jambes complètes, complet, aisselles", time: "1 h 15 min", price: "67€"},
        { name: "Jambes complètes, échancré, aisselles", time: "1 h 05 min", price: "59€"},
        { name: "Cure de 6 séances", time: "1h", price: "420€ - 70€/séance" },
        { name: "Forfait bien être 1h visage + 1h corps", time: "2h", price: "95€" },
        { name: "Forfait Spa 1h visage + 1h corps + gommage corps", time: "2h 30min", price: "125€" },
        { name: "Forfait beauté mains", time: "≈ 2h", price: "95€"},
        { name: "Forfait beauté pieds", time: "≈ 2h", price: "95€"},
        { name: "Forfait beauté mains 1h visage + soin des mains + pose de vernis", time: "≈ 3h", price: "121€"},
        { name: "Forfait beauté pied 1h visage + soins des pieds + pose de vernis", time: "≈ 3h", price: "126€"}


    ];
</script>

<div class="forfaits-page">
    <div class="header-section" style="background-image: url({ForfaitsImage})">
        <div class="overlay"></div>
        <h1>Prestations Forfaits</h1>
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
