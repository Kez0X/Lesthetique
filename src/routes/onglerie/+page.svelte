<svelte:head>
    <title>Onglerie à Domicile - Manucure & Pédicure - L'esthétique</title>
    <meta name="description" content="Profitez de nos services d'onglerie à domicile : manucure, pédicure, pose de vernis classique ou semi-permanent. Disponible à Oullins, Saint-Genis-Laval, Sainte-Foy-lès-Lyon et les alentours." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthetique AA, l'esthétique AA, L'Esthétique AA, Esthetique AA, esthetique AA Oullins, l'esthetiqueAA Oullins, L'EsthetiqueAA Oullins, Esthetique AA Oullins, esthetique à domicile, esthetique AA domicile, l'esthétique AA, esthétique AA, Esthétique AA, L'Esthetique AA, Esthétique AA">

     <script>
        function getCookie(name) {
            const value = `; ${document.cookie}`;
            const parts = value.split(`; ${name}=`);
            if (parts.length === 2) return parts.pop().split(";").shift();
        }

        function loadFbPixel() {
            if (window.fbq) {
                fbq("track", "PageView");
                return;
            }

            !(function(f, b, e, v, n, t, s) {
                if (f.fbq) return;
                n = f.fbq = function () {
                    n.callMethod ? n.callMethod.apply(n, arguments) : n.queue.push(arguments);
                };
                if (!f._fbq) f._fbq = n;
                n.push = n;
                n.loaded = !0;
                n.version = "2.0";
                n.queue = [];
                t = b.createElement(e);
                t.async = !0;
                t.src = "https://connect.facebook.net/en_US/fbevents.js";
                s = b.getElementsByTagName(e)[0];
                s.parentNode.insertBefore(t, s);
            })(window, document, "script");

            fbq("init", "669075309377526");
            fbq("track", "PageView");
        }

        $: {

            if (typeof window !== 'undefined') {
                setTimeout(() => {
					console.log(window.tarteaucitron?.state?.facebookpixel);
                    if (window.tarteaucitron?.state?.facebookpixel === true) {
                        loadFbPixel();
                    }
                }, 500);
            }
        }
    </script>
</svelte:head>

<script>
    import OnglerieImage from '$lib/images/onglerie.png';

    let prestations = [
        { name: "Pose de vernis semi-permanent", time: "≈ 1h30", price: "40€", description: "Cuticules, limage, pose de vernis, huile de fin de soin" },
        { name: "Dépose & semi permanent", time: "≈ 2h", price: "45€", description: "" },
        { name: "Dépose semi permanent", time: "≈ 30min", price: "18€", description: "" },
        { name: "Soin des mains", time: "1h", price: "50€", description: "Gommage, limage, massage, hydratation & base" },
        { name: "Manucure express", time: "35min", price: "30€", description: "limage, soin des ongles, hydratation & base" },
        { name: "Soin des pieds", time: "1h", price: "55€", description: "Gommage, râpe, limage, massage, hydratation et base" },
        { name: "Soin des mains + pose de vernis semi-permanent", time: "≈ 1h30", price: "70€", description: "Gommage, limage, massage, hydratation et base, cuticules, limage, pose de vernis, huile de fin de soin" },
        { name: "Soin des pieds + pose de vernis semi-permanent", time: "≈ 1h30", price: "75€", description: "Gommage, râpe, limage, massage, hydratation et base, cuticules, limage, pose de vernis, huile de fin de soin" }
    ];
</script>

<div class="onglerie-page">
    <!-- Image de fond et titre -->
    <div class="header-section" style="background-image: url({OnglerieImage});">
        <div class="overlay"></div>
        <h1>Prestations Onglerie - Manucure - Pédicure</h1>
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
    <p>Les manucures et pédicures sont réalisées avec des produits bio et/ou naturels. 🍃</p>
    <p>Le semi-permanent est réalisé avec des produits conventionnels.</p>
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
