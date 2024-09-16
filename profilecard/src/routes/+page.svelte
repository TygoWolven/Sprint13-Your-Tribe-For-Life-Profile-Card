<script>
    import trainTrack from "$lib/assets/trainTrack.png"
    import mineCart from "$lib/assets/mineCart.png"
</script>

<section id="home">
    <h2>Wolven Wolven <span>Tygo</span> Wolven Wolven</h2>
    <h2>Tygo Tygo <span>Wolven</span> Tygo Tygo</h2>
    <p>Frontend Developer</p>

    <div class="scrollIcons">
        <a href="#contact">
          <p>Scroll</p>
          <svg width="25px" height="25px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M6 9L12 15L18 9" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </a>
    </div>
</section>

<section id="contact">
    <img alt="The project logo" src={mineCart} />
    <img alt="The project logo" src={trainTrack} />
</section>


<style>
    #contact > img:first-of-type {
        animation: minecartDriving 15s linear infinite;
    }

    @keyframes minecartDriving {
        0% {
            transform: translateX(-100%);
        }   
        100% {
            transform: translateX(100%);
        }
    }

    section {
        width: 100%;
        height: 100vh;
        position: relative;

        display: flex;
        overflow: hidden;
        align-items: center;
        flex-direction: column;
        justify-content: center;

        background-image: linear-gradient(
            to right,
            transparent 48%,
            var(--secondary) 50%,
            transparent 52%
        );
        background-size: 50px;

        & > img {
            position: absolute;
            top: 0;
            left: 0;

            width: 100%;
            height: 100%;

            object-fit: cover;
            pointer-events: none;
        }
    }

    h2 {
        font-size: 10em;
        color: transparent;
        white-space: nowrap;
        text-transform: uppercase;
        -webkit-text-stroke: 5px var(--primary);
    }

    #home > h2:first-of-type {
        margin-right: 25%;
        margin-bottom: -0.5em;
    }

    span {
        color: var(--primary);
    }

    #home > p {
        position: absolute;
        font-size: 3em;
        font-family: Caveat;
        margin-left: 33%;
        margin-top: 9em;
        transition: 0.1s ease;
    }

    #home > p:hover {
        scale: 1.1;
    }

    .scrollIcons {
        position: absolute;
        bottom: 25px;
    }

    .scrollIcons a {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .scrollIcons p {
        text-transform: uppercase;
        animation: textHop 1s infinite;
    }

    .scrollIcons svg:last-of-type {
        position: relative;
        bottom: 3px;
        animation: chevronHop 1s infinite;
    }

    @keyframes textHop {
        0% {
            transform: translateY(0);
        }
        50% {
            transform: translateY(0.5em);
        }
        100% {
            transform: translateY(0);
        }
    }   

    @keyframes chevronHop {
        0% {
            transform: translateY(0);
        }
        60% {
            transform: translateY(0.5em);
        }
        100% {
            transform: translateY(0);
        }
    }
</style>