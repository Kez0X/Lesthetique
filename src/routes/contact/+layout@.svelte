<script>
    import '../../app.css'; // Charge le style global si nécessaire
    import Footer from '$lib/footer.svelte';
    import Back from '$lib/images/background-tree.png';
</script>

<div class="contact-layout" style="background-image: url('{Back}');">
    <slot />
</div>
<Footer />

<style>
    /* Styles globaux pour le corps de la page */
    :global(body) {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
        overflow: hidden; /* Empêche le défilement si nécessaire */
    }

    .contact-layout {
        text-align: center;
        padding: 20px;
        border-radius: 8px;
        width: 100vw;
        height: 100vh;
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        background-attachment: fixed; /* Image fixe lors du défilement */
    }
</style>
