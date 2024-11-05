<svelte:head>
    <title>Épilations - L'esthétique</title>
    <meta name="description" content="Découvrez nos services d'épilation réalisés avec des cires bio certifiées." />
</svelte:head>

<script>
    import EpilationsImage from '$lib/images/epilations.png';

    let prestations = [
        { name: "Sourcils", time: "15 min", price: "14€"},
        { name: "Lèvres", time: "10 min", price: "10€" },
        { name: "Menton", time: "10 min", price: "10€" },
        { name: "Joues", time: "10 min", price: "10€" },
        { name: "Forfaits visage complet", time: "45 min", price: "45€" },
        { name: "Maillot complet", time: "30 min", price: "28€" },
        { name: "1/2 jambes", time: "20 min", price: "20€" },
        { name: "Jambes complètes", time: "30 min", price: "28€" },
        { name: "Aisselles", time: "20 min", price: "20€" },
        { name: "Bras", time: "20 min", price: "20€" }
    ];
</script>

<div class="epilations-page">
    <div class="header-section" style="background-image: url({EpilationsImage})">
        <div class="overlay"></div>
        <h1>Prestations Épilations</h1>
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
