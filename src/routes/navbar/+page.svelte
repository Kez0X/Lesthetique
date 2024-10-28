<script>
	import Instagram from '$lib/images/Instagram.webp';
	import Facebook from '$lib/images/Facebook.png';
</script>

<svelte:head>
	<title>L'esthétique</title>
	<meta name="description" content="" />
</svelte:head>
  
<div class="menu-container">
    <div class="header-container">
        <a href=""><span></span></a>
        <h1>L'esthétiqueAA</h1>
    </div>
    <div class="menu-item" id="1">
        <p>Onglerie</p>
    </div>
    <div class="menu-item" id="2">
        <p>Épilations</p>
    </div>
    <div class="menu-item" id="3">
        <p>Massages</p>
    </div>
    <div class="menu-item" id="4">
        <p>Soins Visages</p>
    </div>
    <div class="menu-item" id="5">
        <p>Réhaussement de Cils</p>
    </div>
    <div class="menu-item" id="6">
        <p>Forfaits</p>
    </div>
    <div class="footer-container">
        <a class="contact" href="">Nous contacter</a>
        <div class="social-icons">
            <a href=""><img src={Facebook} alt="Facebook"></a>
			<a href="https://www.instagram.com/anaisdelice.estheticienne69?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw=="><img src={Instagram} alt="Instagram"></a>
        </div>
    </div>
</div>
  
<style>
    body{
        background : white;
    }
    .menu-container{
        background : white;
        width: 100%;
    }
</style>