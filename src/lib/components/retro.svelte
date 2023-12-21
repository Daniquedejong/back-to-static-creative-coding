    <script>

    </script>

    <section>
    	<svg viewBox="45 -300 1000 600" width="110%" height="100%" xmlns="http://www.w3.org/2000/svg">
            <path
        d="M50 0 Q 100 -50 200 0 Q 300 50 400 0 Q 500 -50 600 0 Q 700 50 800 0 Q 900 -50 950 0"
        stroke="purple"
        stroke-width="50"
        fill="transparent"
    />
    <path
        d="M50 25 Q 100 -25 200 25 Q 300 75 400 25 Q 500 -25 600 25 Q 700 75 800 25 Q 900 -25 950 25"
        stroke="blue"
        stroke-width="50"
        fill="transparent"
    />
    <path
        d="M50 50 Q 100 0 200 50 Q 300 100 400 50 Q 500 0 600 50 Q 700 100 800 50 Q 900 0 950 50"
        stroke="green"
        stroke-width="50"
        fill="transparent"
    />
    <path
        d="M50 75 Q 100 25 200 75 Q 300 125 400 75 Q 500 25 600 75 Q 700 125 800 75 Q 900 25 950 75"
        stroke="yellow"
        stroke-width="50"
        fill="transparent"
    />
    <path
        d="M50 100 Q 100 50 200 100 Q 300 150 400 100 Q 500 50 600 100 Q 700 150 800 100 Q 900 50 950 100"
        stroke="orange"
        stroke-width="50"
        fill="transparent"
    />
    <path
        d="M50 125 Q 100 75 200 125 Q 300 175 400 125 Q 500 75 600 125 Q 700 175 800 125 Q 900 75 950 125"
        stroke="red"
        stroke-width="50"
        fill="transparent"
    />
    	</svg>
    
        <ul>
        <li aria-label="jump jump">
            <div><img src="/assets/clipart120952.png" class="flower" alt="flower" /></div>
          </li>

          <li aria-label="yay">
            <h2 class="text"><span>R</span><span>E</span><span>T</span><span>R</span><span>O</span><span>-</span>
                <span>S</span><span>T</span><span>U</span><span>F</span><span>F</span></h2> 
          </li>

          <li aria-label="wait for it">
            <div class="jumpy"><img src="\assets\gamer-svgrepo-com.svg" class="jumpy" alt="jumpy"></div>
          </li>

        <li aria-label="op en neer">
            <div><img src="\assets\r-is-for-rocket.svg" class="rocket" alt="rocket"></div>
        </li>

    </ul>
    	
    </section>
    
    <style>
    	* {
    		margin: 0;
    		padding: 0;
            box-sizing: border-box;
    	}
    
    	section {
    		background-color: rgb(255, 225, 169);
            position: relative;
    	}
    
    	.flower {
            position: absolute;
    		width: 10em;
            margin-top: -35em;
            animation-name: none;
    	}

        .text {
            margin-left: 20em;
            margin-top: -32em;
            animation-name: none;
        }

        .jumpy {
            width: 10em;
            margin-left: 18em;
            margin-top: 4em;
            animation-name: none;
        }

        .rocket {
            width: 10em;
            margin-top: -6em;
            margin-left: 60em;
            animation-name: none;
            /* transform: rotateY(180deg); */
        }
    
    	path {
    		stroke-dasharray: 150 2;
    		stroke-dashoffset: 1000;
    		animation: dash 60s linear alternate infinite;
    	}
    
    	@keyframes dash {
    		from {
    			stroke-dashoffset: 700;
    		}
    		to {
    			stroke-dashoffset: 0;
    		}
    	}

        
/*************/
/* jump-jump */
/*************/
@keyframes jump-jump-animation {
  0% {
        translate:0em 0em;
		animation-timing-function:ease-out;
		animation-timing-function:cubic-bezier(0.165, 0.840, 0.440, 1.000);
  }
  50% {
    translate:0em -3rem;
		animation-timing-function:ease-in;
		animation-timing-function:cubic-bezier(0.895, 0.030, 0.685, 0.220);
  }
	100% {
    translate:0em 0em;
  }
}

li[aria-label="jump jump"] div {
    animation-name: jump-jump-animation;
    animation-duration: 0.75s;
    animation-iteration-count: infinite;
}




/*******/
/* YAY */
/*******/

@keyframes yay-animation {
  0%{
    scale:1;
  }
  10%{
    translate:0em 0em;
    scale:1.2 .8; 
  }
  20%{
    translate:0em -.25em; 
    scale:.6 1.5;
    color:rgb(83, 31, 255);
  }
  30%{
    translate:0em 0em;
    scale:1.3 .7;
  }
  40%{
    scale:.9 1.1;
  }
  50%{
    scale:1;
  }
  100%{
    scale:1;
  }
}

li[aria-label="yay"] span {
	font-size:2.5rem;
	display:inline-block;
	transform-origin:center bottom;
	animation-name:yay-animation;
	animation-duration:2s;
	animation-iteration-count:infinite;
	animation-play-state:paused;
    color: red;
}

li[aria-label="yay"] span:nth-of-type(1) {
	animation-delay:0s;
}

li[aria-label="yay"] span:nth-of-type(2) {
	animation-delay:.15s;
}

li[aria-label="yay"] span:nth-of-type(3) {
	animation-delay:.3s;
}

li[aria-label="yay"] span:nth-of-type(4) {
	animation-delay:0s;
}

li[aria-label="yay"] span:nth-of-type(5) {
	animation-delay:.15s;
}

li[aria-label="yay"] span:nth-of-type(6) {
	animation-delay:.3s;
}

li[aria-label="yay"] span:nth-of-type(7) {
	animation-delay:0s;
}

li[aria-label="yay"] span:nth-of-type(8) {
	animation-delay:.15s;
}

li[aria-label="yay"] span:nth-of-type(9) {
	animation-delay:.3s;
}

li[aria-label="yay"] span:nth-of-type(10) {
	animation-delay:0s;
}

li[aria-label="yay"] span:nth-of-type(11) {
	animation-delay:.15s;
}


li[aria-label="yay"] span {
	animation-play-state:running;
}



/***************/
/* wait for it */
/***************/
@keyframes wait-for-it-animation {
  0% {
    transform: translate(0, 0);
  }
  
	100% {
	transform: translate(0, -1em);
	}
}

@keyframes traag-animation {
  0% {

  }
  24% {
    translate:2em 0;
		rotate:y 0deg;
  }
	26% {
		translate:2em 0;
	}
	74% {
		translate:-2em 0;
	}

	100% {
	
	}
}

/* Corrigeer de selector naar de gewenste elementen */
li[aria-label="wait for it"] .jumpy {
    /* Voeg de animatie toe aan de gewenste elementen */
    animation-name: wait-for-it-animation, traag-animation;
    animation-duration: 1s, 6s;
    animation-iteration-count: infinite;
    animation-timing-function: ease-out, linear;
    animation-direction: alternate;

}




/**************/
/* op en neer */
/**************/
@keyframes op-en-neer-animation {
  0% {
		translate:0 0;
  }
  50% {
    translate:0 -8em;
  }
	100% {
    translate:0 0;
  }
}

li[aria-label="op en neer"] div {
	width:1em;
	/* aspect-ratio:1; */
	border-radius:50%;
	/* background-color:darkorange; */
}

li[aria-label="op en neer"] div {
  animation-duration:2s;
	animation-iteration-count:infinite;
	animation-timing-function:ease-in-out;
    animation-name:op-en-neer-animation;
}



    </style>
    

