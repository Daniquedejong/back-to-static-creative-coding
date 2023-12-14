next



<style>
section {
    background-image: linear-gradient(to right, #333 1px, transparent 1px),
        linear-gradient(to bottom, #333 1px, transparent 1px);
    background-size: 40px 40px;
}

#cursor2 {
    position: fixed;
    width: 25px;
    height: 25px;
    border-top: 5px solid #0f0;
    border-left: 5px solid #0f0;
    transform-origin: top;
    transform: translate(-1px, 5px) rotate(15deg) scale(0);
    transition: transform 0.1s;
    pointer-events: none;
    animation: animate 5s linear infinite;
}

#cursor2::before {
    content: '';
    position: absolute;
    left: -2.5px;
    width: 5px;
    height: 40px;
    background: #0f0;
    transform-origin: top;
    transform: rotate(315deg);
}

main:hover {
    cursor: none;
}

main:hover #cursor2 {
    transform: translate(-1px, 5px) rotate(15deg) scale(1);
}

@keyframes animate {
    0% {
        filter: drop-shadow(0 0 5px #0f0) drop-shadow(0 0 15px #0f0) drop-shadow(0 0 30px #0f0)
            hue-rotate(0deg);
    }
    100% {
        filter: drop-shadow(0 0 5px #0f0) drop-shadow(0 0 15px #0f0) drop-shadow(0 0 30px #0f0)
            hue-rotate(360deg);
    }
}

</style>