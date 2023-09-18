<script lang="ts">
	
	let currentSlide = 0;
	const slides = ['/assets/inscription.png', '/assets/LogoGood.png', '/assets/Logogoogle.png'];
  
	function nextSlide() {
	  currentSlide = (currentSlide + 1) % slides.length;
	}
  
	function prevSlide() {
	  currentSlide = (currentSlide - 1 + slides.length) % slides.length;
	}
  </script>
  
  <section>
	<article id="tuto">
	  <h1>Présentation de l'application RenconSport :</h1>
  
	  <div id="caroussel" class="carousel-container">
		<button class="carousel-button prev" on:click={prevSlide}>◀</button>
		<div class="carousel">
		  {#each slides as slide, i}
			<div class="slide">
			  <img src={slide} alt={`Slide ${i + 1}`} />
			</div>
		  {/each}
		</div>
		<button class="carousel-button next" on:click={nextSlide}>▶</button>
	  </div>
	</article>
  </section>
  
  <style>
	section {
	  height: 100vh;
	  background-color: #eeecde;
	}
	h1 {
	  font-weight: lighter;
	  font-size: 1.5rem;
	  color: #7faac8;
	}
	.carousel-container {
	  display: flex;
	  justify-content: center;
	  align-items: center;
	  position: relative;
	  
	}
  
	.carousel-button {
	  position: absolute;
	  top: 50%;
	  transform: translateY(-50%);
	  background-color: #7faac8;
	  border: none;
	  color: white;
	  font-size: 1.5rem;
	  cursor: pointer;
	  padding: 10px;
	  border-radius: 50%;
	  transition: background-color 0.3s ease;
	}
  
	.carousel-button:hover {
	  background-color: #5588a3;
	}
  
	.prev {
	  left: 10px;
	}
  
	.next {
	  right: 10px;
	}
  
	.carousel {
	  display: flex;
	  overflow: hidden;
	  width: 100%;
	  
	}
  
	.slide {
	  min-width: 100%;
	  display: flex;
	  justify-content: center;
	  align-items: center;
	  transition: transform 0.5s ease;
	
	}
  
	img {
	  max-width: 100%;
	  max-height: 60%;

	}
  
	@media screen and (max-width: 600px) {
	  img {
		max-height: 80vh;
	  }
	}
  </style>
  