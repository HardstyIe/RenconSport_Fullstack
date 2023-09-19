<script></script>
<nav>
    <div class="logo">
        <img src="/assets/LogoGood.png" alt="Renconsport Logo">
    </div>
</nav>

<style>
nav {
    background: rgb(249,249,249);
    background: radial-gradient(circle, rgba(249,249,249,1) 22%, rgba(165,206,235,1) 46%, rgba(127,170,200,1) 76%);
    display: flex;
    justify-content: space-between; /* Pour séparer les logos à gauche et à droite */
    align-items: center; /* Pour centrer verticalement les logos */
    height: 10vh;
    padding: 0 20px; /* Espace autour des logos pour les séparer du bord de la navbar */
    box-shadow: red 15px 15px 105px;
}

.logo {
    height: 110%;
}

img {
    height: 90%; 
}



@media screen and (max-width: 800px) {
    .logo {
        margin: auto;
    }
}

</style>
