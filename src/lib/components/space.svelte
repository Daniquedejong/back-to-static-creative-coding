<script>
	import { onMount } from "svelte";


    onMount(() => {

    let cursor = document.querySelector('#cursor');
    let body = document.querySelector('body');
    document.addEventListener('mousemove', (e) => {
    body.style.backgroundPositionX = e.pageX/-4 + 'px';
    body.style.backgroundPositionY = e.pageY/-4 + 'px';
    cursor.style.top = e.pageY + 'px';
    cursor.style.left = e.pageX + 'px';
})

    });
    

</script>

<section>
<body>
    
      <nav class="footer">
    
      <a href="/"><img src="assets\visual-thinking-logo-footer.svg" class="logo-footer" alt="footer-logo"></a>
    
      <ul class="footer-menu">
        <h4>
        <a href="/over" ><li>Over</li></a>
        <a href="/artikelen" ><li>Artikelen</li></a>
        <a href="/tekenmethodes" ><li>Tekenmethodes</li></a>
        <a href="/kennisclips" ><li>Kennisclips</li></a>
        </h4>
      </ul>
    
      <ul class="social-media">
      <h4>Contact</h4>
      <a href="https://www.instagram.com/charley_muhren/"><img src="assets\instagram.svg" alt="instagram"></a>
      <a href="https://www.youtube.com/playlist?list=PLjrep0WCM97y9fznRYBVVKyDkzlT9fWEa"><img src="assets\youtube.svg" alt="youtube"></a> 
      <a href="https://www.linkedin.com/in/charleymuhren/"><img src="assets\iconmonstr-linkedin-3.svg" alt="linkedIn"></a>
      <h5>© Charley Muhren, 2022</h5>
      </ul>
    
      </nav>

      <div id="cursor"></div>

    </body>
</section>

<style>

    :root {
        --vtPrimaryFont: "rigid-square", sans-serif;
        --vtSecondaryFont: "yrsa", serif;
        --vtDarkBlue: #090940;
    }

    body {
        background-image: linear-gradient(to right, #333 1px,
        transparent 1px), linear-gradient(to bottom, #333 1px,
        transparent 1px);
        background-size: 40px 40px;
    }

    #cursor {
        position: fixed;
        width: 25px;
        height: 25px;
        border-top: 5px solid #0f0;
        border-left: 5px solid #0f0;
        transform-origin: top;
        transform: translate(-1px, 5px)rotate(15deg) scale(0);
        transition: transform 0.1s;
        pointer-events: none;
        animation: animate 5s linear infinite;
    }

    #cursor::before {
        content: '';
        position: absolute;
        left: -2.5px;
        width: 5px;
        height: 40px;
        background: #0f0;
        transform-origin: top;
        transform: rotate(315deg);
    }

    body:hover #cursor {
        transform: translate(-1px, 5px)rotate(15deg) scale(1);
    }

    @keyframes animate {
        0% {
            filter: drop-shadow(0 0 5px #0f0) drop-shadow(0 0 15px #0f0)
            drop-shadow(0 0 30px #0f0) hue-rotate(0deg);
        }
        100% {
            filter: drop-shadow(0 0 5px #0f0) drop-shadow(0 0 15px #0f0)
            drop-shadow(0 0 30px #0f0) hue-rotate(360deg);  
        }
    }
    
    .footer {
        display: grid;
        grid-template-columns: repeat(3, 1fr); 
        align-items: center;
        gap: 10px; 
        background-color: rgb(240, 240, 240);
        font-family: var(--vtPrimaryFont);
        padding: 2em;
    }
    
    a {
        text-decoration: none;
        color: var(--vtDarkBlue);
    }
    
    li {
        list-style-type: none;
        margin-bottom: 0.5em;
    }
    
    img {
        grid-column: 1;
        margin-right: 1em;
    }
    
    .logo-footer {
        width: 16em;
        margin-left: 6em;
    }
    
    .footer-menu {
        grid-column: 2;
        margin-left: 5em;
    }
    
    .social-media {
        grid-column: 3;
        
    }
    
    @media (max-width: 920px) { 
    .footer {
        display: grid;
        grid-template-columns: repeat(1, 1fr); 
        grid-template-rows: repeat(3, 1fr);
        align-items: center;
        gap: 10px;
        margin-left: 1em;
    }
    
    img {
        grid-column: 1;
        grid-row: 1;
    }
    
    .footer-menu {
        grid-column: 1;
        grid-row: 2;
    }
    
    .social-media {
        grid-column: 1;
        grid-row: 3;
    }
    }

</style>