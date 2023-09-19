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
    "Page inscriptions :   Si vous êtes nouveau, commencez par créer un compte avec votre email.",
    "Page connexion : connectez vous avec les identifiants que vous avez utilisé pour vous inscrire.",
    "Page acceuil : sur la page principale, vous verrez les profils d'autres utilisateurs. Swipez vers la gauche si vous n'êtes pas intéressé(e) et vers la droite si vous l'êtes. Si quelqu'un que vous avez aimé aime aussi votre profil, c'est un match ! ",
    "Page profil : Vous arrivez sur votre profil ou vous retrouver vos informations avec votre pseudo , votre age , vos etudes , vos sports pratiqués et une bréve description",
    "Page entrainements : Sur la page entrainement vous aurez acces a toutes les seances d'entrainement disponible.",
    "Page detail d'un entrainement : Sur la page detail d'un entrainement vous aurez acces a tout les details de l'activités choisis (lieu, heure, date...) ",
    "Page messagerie : Sur la page messagerie vous pourrez directement communniquer avec les personnes avec lesquels vous avez matché.",
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
    width: 100vw;
    height: 70vh;
    margin: auto;
  }

  .slide {
    text-align: center;
    max-width: 100%;
  }

  .slide img {
    border-radius: 30px;
  }

  img {
    max-width: 100%;
    height: auto; /* Ajustement automatique de la hauteur */
    max-height: 400px; /* Hauteur maximale de l'image */
  }

  p {
    font-family: 'Montserrat', sans-serif;
    position: relative;
    top: 5px;
    font-size: 1.2rem;
    max-width: 100%;
    padding: 0 1%;
    margin: auto;
    margin-top: 20px; 
    margin-bottom: 20px; 
    
  }

  button {
    position: absolute;
    top: 42%;
    transform: translateY(-50%);
    background-color: #404041;
    color: white;
    border: none;
    font-size: 24px;
    cursor: pointer;
    margin: 0 15px;
    padding: 12px 24px;
    border-radius: 50%;
  }

  button:hover {
    opacity: 0.9;
  }

  button:first-child {
    left: 0;
  }

  button:last-child {
    right: 0;
  }

  h1 {
    font-family: 'Merriweather', serif;
    text-align: center;
    text-transform: uppercase;
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
      font-family: 'Montserrat', sans-serif;
      font-size: 16px; 
    }

    
  }

  @media screen and (max-width: 600px) {

    button {
      border-radius: 0px;
      margin: 2px;
      padding: 5px 5px;
    }

  }
</style>
