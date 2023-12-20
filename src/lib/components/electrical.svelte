<script>
// Importeert functies van Svelte
import { onMount } from 'svelte';
  
// Initialiseren van variabelen
  let isAnimating = false;
  let svgElement;
  let carousel;

  // Als pagina is geladen,
  // dan zoeken naar deze specifieke elementen
  onMount(() => {
    svgElement = document.querySelector('.lamp');
    carousel = document.querySelector('.carousel');
  });

  // Funtie om SVG te wijzigen --> 
  // verandert de bron van SVG
  function changeSVG() {
    svgElement.src = 'assets/free_icon_1 (1).svg';
  }

  // Functie om carouselanimatie te starten --> 
  // voegt een class toe om de animatie te laten draaien
  function triggerCarouselAnimation() {
    carousel.classList.add('animate-carousel');
  }

  // Funtie om de carouselanimatie te stoppen -->
  // verwijdert class om animatie te laten stoppen
  function stopCarouselAnimation() {
  carousel.classList.remove('animate-carousel');
}

  // Functie om te klikken -->
  // verandert de SVG bron
  // controleert of de animatie aan het draaien is
  // als hij draait dan stopt de animatie
  // anders start het de animatie
  function handleClick() {
	changeSVG();
  if (isAnimating) {
    stopCarouselAnimation();
    isAnimating = false;
  } else {
    triggerCarouselAnimation();
    isAnimating = true;
  }
  }
</script>

<section>
	<main>
		<!-- Carousel -->
		<div class="container">
			<div class="carousel">
				<!-- Class voor true of false voor button click -->
				<div class={isAnimating ? "carousel animate-carousel" : "carousel"}>
				<a href="/over" class="carousel__face"
					><span>Over visual thinking</span><img src="assets\arrows.svg" alt="arrow" class="arrow" />
				</a>
				<a href="/kennisclips" class="carousel__face"
					><span>Kennisclips</span> <br /><img src="assets\arrows.svg" alt="arrow" class="arrow"/>
				</a>
				<a href="/minicursussen" class="carousel__face"
					><span>Minicursussen</span><img src="assets\arrows.svg" alt="arrow" class="arrow"/>
				</a>
				<a href="/tekenmethodes" class="carousel__face"
					><span>Visual thinking methodes</span><img src="assets\arrows.svg" alt="arrow" class="arrow"/>
				</a>
				<a href="/artikelen" class="carousel__face"
					><span>Artikelen</span><img src="assets\arrows.svg" alt="arrow" class="arrow"/>
				</a>
				<a href="/tekenruimte" class="carousel__face"
					><span>Tekenruimte</span><img src="assets\arrows.svg" alt="arrow" class="arrow"/>
				</a>
			</div>
		</div>
	</div>
		<!-- Eerste svg voor de button klik -->
		<img src="assets/free_icon_1.svg" alt="lamp" class="lamp" />
	
		<!-- Button voor verandering -->
		<button on:click={handleClick}>Start</button>
	
	</main>
</section>

<style>

	/* * {
		border: solid 1px red;
	} */

	/*--ROOTS--*/
	:root {
		font-size: 20px;

		--vtDarkBlue: #090940;
		--vtLightBlue: #67c5d1;
		--vtYellow: #feb51e;
		--vtRed: #f96c4f;
		--vtWhite: #ffffff;
		--vtGrey-50: #e0dedc;
		--vtGrey-80: #c0beb9;

		--vtPrimaryFont: 'rigid-square', sans-serif;
		--vtSecondaryFont: 'yrsa', serif;
	}

	main {
		min-height: 25em;
	}

	.arrow {
		width: 2em;
		margin-left: 6.5em;
		margin-top: 9em;
		position: absolute;
	}

	.lamp {
		position: absolute;
		Width: 2em;
		margin-left: 60em;
		margin-top: 18em;
	}

	button {
		margin-left: 18em;
		margin-top: 28em;
		padding: 1.5em;
		clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
		border-style: none;
		font-family: var(--vtPrimaryFont);
		font-weight: 600;
		background-color: var(--vtGrey-80);
		color: var(--vtDarkBlue);
	}

	button:hover {
		background-color: var(--vtYellow);
		color: var(--vtWhite);
	}

	a {
		text-decoration: none;
	}
	
 	/*--CAROUSEL--*/
	.container {
		position: relative;
		width: 320px;
		margin: 10px auto 0 auto;
		perspective: 1000px;
	}

	.carousel {
		position: absolute;
		width: 100%;
		height: 100%;
		transform-style: preserve-3d;
	}

	.animate-carousel {
		animation: rotate360 60s infinite forwards linear;
	}

	.carousel__face {
		position: absolute;
		width: 300px;
		height: 275px;
		top: 20px;
		left: 10px;
		right: 10px;
		background-size: cover;
		box-shadow: inset 0 0 0 2000px rgba(129, 129, 129, 0.5);
		display: flex;
		clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
		transform: rotate(90deg);
	}

	span {
		margin: auto;
		font-size: 18px;
		color: var(--vtWhite);
		font-family: var(--vtPrimaryFont);
		break-after: always;
		display: block;
	}

	span:hover {
		text-transform: uppercase;
	}

	.carousel__face:nth-child(1) {
		background-color: var(--vtDarkBlue);
		transform: rotateY(60deg) translateZ(275px);
	}
	.carousel__face:nth-child(2) {
		background-color: var(--vtLightBlue);
		transform: rotateY(120deg) translateZ(275px);
	}
	.carousel__face:nth-child(3) {
		background-color: var(--vtRed);
		transform: rotateY(180deg) translateZ(275px);
	}
	.carousel__face:nth-child(4) {
		background-color: var(--vtYellow);
		transform: rotateY(240deg) translateZ(275px);
	}
	.carousel__face:nth-child(5) {
		background-color: var(--vtGrey-50);
		transform: rotateY(300deg) translateZ(275px);
	}
	.carousel__face:nth-child(6) {
		background-color: var(--vtGrey-50);
		transform: rotateY(360deg) translateZ(275px);
	}
 	/*--KEYFRAMES--*/
	@keyframes rotate360 {
		from {
			transform: rotateY(0deg);
		}
		to {
			transform: rotateY(360deg);
		}
	}

</style>
