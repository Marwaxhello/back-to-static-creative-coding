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
  <!-- <div class="content">
    <h2 class="text-shadows">Hey</h2>
  </div> -->
</body>

<style>
  @import url("https://fonts.googleapis.com/css?family=Playfair+Display:900");

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

    --vtPrimaryFont: "rigid-square", sans-serif;
    --vtSecondaryFont: "yrsa", serif;
  }

  body {
    /* background-color: var(--vtYellow-80); */
    /* font-family: "Playfair Display", "Georgia", serif; */
    /* font-family: var(--vtSecondaryFont); */
    font-family: var(--vtPrimaryFont);
    margin: 0;
    padding: 0;
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

  .visual-thinking-logo {
    max-width: 100px;
    height: auto;
    margin: 1em;
  }

  header {
    text-align: center;
    background-color: var(--vtYellow-30);
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

  :root {
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
  }
</style>
