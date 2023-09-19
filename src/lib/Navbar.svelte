<script></script>
<nav>
    <div class="logo">
        <img src="/assets/LogoGood.png" alt="Renconsport Logo">
    </div>
</nav>

<style>
nav {
    background-color: #7FAAC8;
    display: flex;
    justify-content: space-between; /* Pour séparer les logos à gauche et à droite */
    align-items: center; /* Pour centrer verticalement les logos */
    height: 80px;
    padding: 0 20px; /* Espace autour des logos pour les séparer du bord de la navbar */
    box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.8); /* Augmentez la taille de l'ombre */
}

.logo {
    height: 90px;
}

img {
    height: 90%; 
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
