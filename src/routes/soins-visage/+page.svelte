<svelte:head>
    <title>Soins du Visage Bio - Esthéticienne à Domicile - L'esthétique AA</title>
    <meta name="description" content="Découvrez nos soins du visage à base de produits bio de la marque ClaireJoie. Offrez à votre peau un moment de douceur et de bien-être avec nos soins personnalisés, disponibles à domicile à Oullins, Saint-Genis-Laval, Sainte-Foy-lès-Lyon, et alentours." />
    <meta name="keywords" content="épilation bio, épilation à domicile, soins de beauté bio, épilation Oullins, épilation Saint-Genis-Laval, épilation Lyon, esthetique AA, l'esthétique AA, L'Esthétique AA, Esthetique AA, esthetique AA Oullins, l'esthetiqueAA Oullins, L'EsthetiqueAA Oullins, Esthetique AA Oullins, esthetique à domicile, esthetique AA domicile, l'esthétique AA, esthétique AA, Esthétique AA, L'Esthetique AA, Esthétique AA">

     <script>
        function getCookie(name) {
            const value = `; ${document.cookie}`;
            const parts = value.split(`; ${name}=`);
            if (parts.length === 2) return parts.pop().split(";").shift();
        }

        function loadFbPixel() {
            if (window.fbq) return;

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
    import SoinsVisagesImage from '$lib/images/soins-visages.png';

    let prestations = [
        { name: "Nettoyage de peau personnalisé", time: "1h", price: "50€", description : "" },
        { name: "Relaxant", time: "30min", price: "35€", description : "Massage relaxant" },
        { name: "Relaxant", time: "1h", price: "50€", description : "Massage relaxant" }
    ];
</script>

<div class="soins-visages-page">
    <div class="header-section" style="background-image: url({SoinsVisagesImage})">
        <div class="overlay"></div>
        <h1>Prestations Soins du Visage</h1>
    </div>

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
    <p>Les soins du visage sont réalisés avec des produits bio français de la marque ClaireJoie. 🍃</p>
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
