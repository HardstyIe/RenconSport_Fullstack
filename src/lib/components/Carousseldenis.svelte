<script>
  let images = [
    '/assets/inscription.png',
    '/assets/Heroe.jpg',
    '/assets/logoapple.png',
    '/assets/LogoGood.png',
    '/assets/logogoogle.png',
    '/assets/LogoGood.png',
    '/assets/LogoGood.png',
  ];

  let captions = [
    "Page inscriptions :   Si vous êtes nouveau, commencez par créer un compte avec votre email ",
    "Page connexion : connectez vous avec les identifiants que vous avez utilisé pour vous inscrire",
    "Page acceuil : Sur la page principale, vous verrez les profils d'autres utilisateurs. Swipez vers la gauche si vous n'êtes pas intéressé(e) et vers la droite si vous l'êtes Si quelqu'un que vous avez aimé aime aussi votre profil, c'est un match ! ",
    "Page profil : Vous arrivez sur votre profil ou vous retrouver vos informations avec votre pseudo , votre age , vos etudes , vos sports pratiqués et une bréve description",
    "Page entrainements : Sur la page entrainement vous aurez acces a toutes les seances d'entrainement disponible ",
    "Page detail d'un entrainement : Sur la page detail d'un entrainement vous aurez acces a tout les details de l'activités choisis (lieu , heure ,date...) ",
    "Page messagerie : Sur la page messagerie vous pourrez directement communniquer avec les personnes avec lesquels vous avez matché ",
    // Ajoutez plus de légendes ici
  ];

  let currentIndex = 0;

  function nextSlide() {
    currentIndex = (currentIndex + 1) % images.length;
  }

  function prevSlide() {
    currentIndex = (currentIndex - 1 + images.length) % images.length;
  }
</script>

<h1>Pour bien commencer</h1>
<div class="slider">
  <button on:click={prevSlide}>&#10094;</button>
  <div class="slide">
    <img src={images[currentIndex]} alt="Slide" />
    <p>{captions[currentIndex]}</p>
  </div>
  <button on:click={nextSlide}>&#10095;</button>
</div>

<style>
  .slider {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    width: 100%;
    max-width: 800px; /* Largeur maximale du slider */
    margin: auto;
    box-shadow: 15px 10px 10px 15px red;
  }

  .slide {
    text-align: center;
    max-width: 100%;
    padding: 0 20px; /* Espacement autour du contenu */
  }

  img {
    max-width: 100%;
    height: auto; /* Ajustement automatique de la hauteur */
    max-height: 400px; /* Hauteur maximale de l'image */
  }

  p {
    font-size: 18px;
    max-width: 100%;
    margin: auto;
    box-shadow: 10px 15px 15px black;
    margin-top: 20px; 
    margin-bottom: 20px; 
    
  }

  button {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    font-size: 24px;
    cursor: pointer;
    padding: 8px 16px;
    border-radius: 4px;
  }

  button:hover {
    background-color: rgba(0, 0, 0, 0.7);
  }

  button:first-child {
    left: 0;
  }

  button:last-child {
    right: 0;
  }

  h1 {
    text-align: center;
    font-size: 3rem;
    margin-bottom: 20px; /* Espacement inférieur réduit */
    margin-top: 20px; /* Espacement supérieur réduit */
  }

  @media screen and (max-width: 600px) {
    /* Styles pour les écrans de moins de 600px de large */
    .slider {
      padding: 0 10px; /* Espacement réduit sur les côtés */
    }
    img {
      max-height: 300px; 
    }
    p {
      font-size: 16px; 
    }
  }
</style>
