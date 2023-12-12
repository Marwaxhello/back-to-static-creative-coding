<script>

  import { onMount } from "svelte";

  let stars = [];

  const rand = (min, max) => Math.floor(Math.random() * (max - min + 1)) + min;

  const animate = star => {
    star.style.setProperty("--star-left", `${rand(-10, 100)}%`);
    star.style.setProperty("--star-top", `${rand(-40, 80)}%`);

    star.style.animation = "none";
    star.offsetHeight;
    star.style.animation = "";
  };

  // Simulate the creation of stars
  onMount(() => {
    stars = Array.from(document.getElementsByClassName("magic-star"));

    stars.forEach((star, index) => {
      setTimeout(() => {
        animate(star);
        setInterval(() => animate(star), 1000);
      }, index * (1000 / 3));
    });
  });
  




</script>


<header>
  <a href="/">
    <img
      src="assets\vtHBO-v1.0-Logo_1.svg"
      class="visual-thinking-logo"
      alt="visual-thinking-logo"
    />
  </a>

  <nav>
    <ul>
      <li><a href="#Tekenmethodes">Tekenmethodes</a></li>
      <li><a href="#Artikelen">Artikelen</a></li>
      <li><a href="#Kennisclips">Kennisclips</a></li>
      <li><a href="#Tekenruimte">Tekenruimte</a></li>
    </ul>
  </nav>
</header>

<body>

<h2>
  Bubblegum
  <span class="magic">

    <span class="magic-star">
      <svg viewBox="0 0 512 512">
      <path d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z" />
      </svg>
    </span>

    <span class="magic-star">
      <svg viewBox="0 0 512 512">
      <path d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z" />
      </svg>
    </span>

    <span class="magic-star">
      <svg viewBox="0 0 512 512">
      <path d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z" />
      </svg>
    </span>  
</h2>

</body>

<style>
  /* @import url("https://fonts.googleapis.com/css?family=Playfair+Display:900"); */
  /* @import url("https://fonts.cdnfonts.com/css/bubblegum"); */
  /* @import url("https://fonts.googleapis.com/css?family=Sacramento"); */
  @import url("https://fonts.cdnfonts.com/css/neko-neco");

  :root {
    /* Visual Thinking: Primary Colors: Zie kleuren styleguide of eventueel Figma designs voor gebruik! */

    --vtDarkBlue: #090940;
    --vtLightBlue: #67c5d1;
    --vtYellow: #feb51e;
    --vtRed: #f96c4f;
    --vtWhite: #ffffff;

    /* Visual Thinking: Primary Colors Lichtere versies, ongeveer 80%, 50%, 30% en 10% opacity van de originele kleuren ^
    Zie kleuren styleguide of eventueel Figma designs voor gebruik!  */

    --vtDarkBlue-80: #3a3a66;
    --vtDarkBlue-50: #6b6b8c;
    --vtDarkBlue-30: #9d9db3;
    --vtDarkBlue-10: #ceced9;

    --vtLightBlue-80: #85d1da;
    --vtLightBlue-50: #a4dce3;
    --vtLightBlue-30: #c2e8ed;
    --vtLightBlue-10: #e1f3f6;

    --vtYellow-80: #fec44b;
    --vtYellow-50: #fed378;
    --vtYellow-30: #ffe1a5;
    --vtYellow-10: #fff0d2;

    --vtRed-80: #fa8972;
    --vtRed-50: #fba795;
    --vtRed-30: #fdc4b9;
    --vtRed-10: #fee2dc;
    --ccPink-bubblegum-bg: #fce8eb;
    --ccPink-bubblegum: #ffaed7;

    --vtPrimaryFont: "rigid-square", sans-serif;
    --vtSecondaryFont: "yrsa", serif;
  }

  body {
    /* background-color: var(--vtYellow-80); */
    /* font-family: "Playfair Display", "Georgia", serif; */
    /* font-family: var(--vtSecondaryFont); */
    font-family: var(--vtPrimaryFont);
    background-color: var(--ccPink-bubblegum-bg);
    margin: 0;
    padding: 0;

   /* display: grid;
   height: 100vh;
   overflow: hidden;
   place-items: center; */
  }

  .visual-thinking-logo {
    max-width: 100px;
    height: auto;
    margin: 1em;
  }

  header {
    text-align: center;
    background-color: var(--ccPink-bubblegum);
    padding: 10px;
  }

  nav {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  li {
    display: inline-block;
    margin-right: 40px;
    transition: transform 4s ease-in-out;
    margin-bottom: 2em;
  }

  a {
    text-decoration: none;
    color: var(--vtDarkBlue);
    font-weight: bold;
    font-size: 20px;
  }

  /* li:hover,
  a:hover {
    transform: scale(2.5); /* Adjust the scale factor as needed */
  /* transition: transform 4s ease-in-out; */

  /* :root {
    --color-primary: #f6aca2;
    --color-secondary: #f49b90;
    --color-tertiary: #f28b7d;
    --color-quaternary: #f07a6a;
    --color-quinary: #ee6352;
  }

  li:hover,
  a:hover {
    text-shadow:
      3px 3px 0 var(--color-secondary),
      6px 6px 0 var(--color-tertiary),
      9px 9px var(--color-quaternary),
      12px 12px 0 var(--color-quinary);
    font-size: 20px;
    margin-right: 40px;
    text-align: center;
    margin: 0;
    color: var(--color-primary);
    animation: shadows 4s ease-in infinite;
  }

  @keyframes shadows {
    0% {
      text-shadow: none;
    }
    10% {
      transform: translate(-3px, -3px);
      text-shadow: 3px 3px 0 var(--color-secondary);
    }
    20% {
      transform: translate(-6px, -6px);
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary);
    }
    30% {
      transform: translate(-9px, -9px);
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary);
    }
    40% {
      transform: translate(-12px, -12px);
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary),
        12px 12px 0 var(--color-quinary);
    }
    50% {
      transform: translate(-12px, -12px);
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary),
        12px 12px 0 var(--color-quinary);
    }
    60% {
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary),
        12px 12px 0 var(--color-quinary);
    }
    70% {
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary);
    }
    80% {
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary);
    }
    90% {
      text-shadow: 3px 3px 0 var(--color-secondary);
    }
    100% {
      text-shadow: none;
    }
  } */

  /* BUBBLEGUM CREATIVE CODING #2 */

  h2 {
    /* font-family: 'BubbleGum', sans-serif; */
    /* font-family: 'Sacramento'; */
    font-family: "Neko Neco", sans-serif;
    color: var(--ccPink-bubblegum);
    text-align: center;
    margin: 2em;
    font-size: 50px;
  }


/* STARS ANIMATION */

@keyframes scale {
  from, to {
    transform: scale(0);
  }
  
  50% {
    transform: scale(1);
  }
}

@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  
  to {
    transform: rotate(180deg);
  }
}

h2 > .magic {
  display: inline-block;
  position: relative;
}

h2 > .magic > .magic-star {
  --size: clamp(20px, 1.5vw, 30px);
  animation: scale 700ms ease forwards;
  display: block;
  height: var(--size);
  left: var(--star-left);
  position: absolute;
  top: var(--star-top);
  width: var(--size);
}

h2 > .magic > .magic-star > svg {
  animation: rotate 1000ms linear infinite;
  display: block;
  opacity: 0.7;
}

h2 > .magic > .magic-star > svg > path {
  fill: var(--vtWhite);
}




  /* 3D ANIMATION */

  /* *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  :root {
    --color-primary: #f6aca2;
    --color-secondary: #f49b90;
    --color-tertiary: #f28b7d;
    --color-quaternary: #f07a6a;
    --color-quinary: #ee6352;
  }

  body {
    min-height: 100vh;
    font-weight: 300;
    font-size: 1.25rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    overflow: hidden;
    background-color: #eff8e2;
  }

  .content {
    display: flex;
    align-content: center;
    justify-content: center;
  }

  .text-shadows {
    text-shadow:
      3px 3px 0 var(--color-secondary),
      6px 6px 0 var(--color-tertiary),
      9px 9px var(--color-quaternary),
      12px 12px 0 var(--color-quinary);
    font-family: bungee, sans-serif;
    font-weight: 400;
    text-transform: uppercase;
    font-size: calc(2rem + 5vw);
    text-align: center;
    margin: 0;
    color: var(--color-primary);
    animation: shadows 4s ease-in infinite;
    letter-spacing: 0.4rem;
  }

  @keyframes shadows {
    0% {
      text-shadow: none;
    }
    10% {
      transform: translate(-3px, -3px);
      text-shadow: 3px 3px 0 var(--color-secondary);
    }
    20% {
      transform: translate(-6px, -6px);
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary);
    }
    30% {
      transform: translate(-9px, -9px);
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary);
    }
    40% {
      transform: translate(-12px, -12px);
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary),
        12px 12px 0 var(--color-quinary);
    }
    50% {
      transform: translate(-12px, -12px);
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary),
        12px 12px 0 var(--color-quinary);
    }
    60% {
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary),
        12px 12px 0 var(--color-quinary);
    }
    70% {
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary),
        9px 9px var(--color-quaternary);
    }
    80% {
      text-shadow:
        3px 3px 0 var(--color-secondary),
        6px 6px 0 var(--color-tertiary);
    }
    90% {
      text-shadow: 3px 3px 0 var(--color-secondary);
    }
    100% {
      text-shadow: none;
    }
  }  */
</style>

