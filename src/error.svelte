<script>
    export let status; // Code d'erreur (404, 502, etc.)
    export let error;  // Message d'erreur optionnel

    // Messages d'erreur personnalisés en fonction du code d'erreur
    let errorMessages = {
        404: {
            title: "Page non trouvée",
            message: "La page que vous recherchez n'existe pas ou a été déplacée."
        },
        502: {
            title: "Mauvaise passerelle",
            message: "Il semble qu'il y ait un problème de communication avec le serveur. Veuillez réessayer plus tard."
        },
        500: {
            title: "Erreur serveur interne",
            message: "Une erreur s'est produite sur le serveur. Nous travaillons pour la corriger."
        },
        403: {
            title: "Accès refusé",
            message: "Vous n'avez pas la permission d'accéder à cette page."
        },
        default: {
            title: "Oups!",
            message: "Une erreur est survenue. Veuillez réessayer ou revenir plus tard."
        }
    };

    // Récupérer le message approprié pour le statut d'erreur
    let errorMessage = errorMessages[status] || errorMessages.default;
</script>

<div class="error-page">
    <h1>{errorMessage.title}</h1>
    <p>{errorMessage.message}</p>
    {#if error}
        <p class="error-detail">{error.message}</p>
    {/if}
    <a href="/" class="home-link">Retour à l'accueil</a>
</div>

<style>
    .error-page {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100vh;
        text-align: center;
        color: #333;
        font-family: Arial, sans-serif;
        background-color: #fdf6f9;
        padding: 20px;
    }

    h1 {
        font-size: 2.5em;
        color: #d45a72;
    }

    p {
        font-size: 1.2em;
        color: #555;
        margin: 10px 0;
    }

    .error-detail {
        color: #999;
        font-size: 0.9em;
    }

    .home-link {
        display: inline-block;
        margin-top: 20px;
        padding: 10px 20px;
        background-color: #d45a72;
        color: white;
        text-decoration: none;
        border-radius: 5px;
        transition: background-color 0.3s;
    }

    .home-link:hover {
        background-color: #b04359;
    }
</style>
