<script></script>
<nav>
    
        <div class="left-logo">
            <img src="/assets/LogoGood.png" alt="Renconsport Logo">
        </div>
        <div class="right-logos">
            <img src="/assets/logoapple.png" alt="Logo Apple store">
            <img src="/assets/logogoogle.png" alt="Logo Google Play Store">
        </div>
    
    
</nav>


<style>
nav {
    background-color: #7FAAC8;
    display: flex;
    justify-content: space-between; /* Pour séparer les logos à gauche et à droite */
    align-items: center; /* Pour centrer verticalement les logos */
    height: 150px;
    padding: 0 20px; /* Espace autour des logos pour les séparer du bord de la navbar */
}

.right-logo {
    order: 1; 
}

.left-logos {
    display: flex;
    gap: 10px; 
}

img {
    height: 100%; 
}

@media screen and (max-width: 600px) {
    nav {
        height: 100px;
    }
    
    img {
        height: 80px; /* Réduit la taille des logos pour les écrans plus petits */
    }
}


@media screen and (max-width: 600px) {
    nav {
        height: 100px;
    }

    img {
        height: 100px;
    }
}

@media screen and (min-width: 601px) and (max-width: 1024px) {
    nav {
        height: 100px;
    }

    img {
        height: 100px;
    }
}

@media screen and (min-width: 1025px) and (max-width: 1440px) {
    nav {
        height: 150px;
    }

    img {
        height: 150px;
    }
}



</style>
