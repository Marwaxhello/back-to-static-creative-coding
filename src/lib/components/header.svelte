<script>

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


<style>
  @import url("https://fonts.googleapis.com/css?family=Playfair+Display:900");
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
    /* font-family: "Playfair Display", "Georgia", serif; */
    /* font-family: var(--vtSecondaryFont); */
    font-family: var(--vtPrimaryFont);
    background-color: var(--ccPink-bubblegum-bg);
    margin: 0;
    padding: 0;
    overflow: hidden;
  }

  .visual-thinking-logo {
    max-width: 100px;
    height: auto;
    margin: 1em;
  }

  header {
    text-align: center;
    font-family: var(--vtPrimaryFont);
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

  /* BUBBLEGUM CREATIVE CODING #2 */

  h2 {
    font-family: "Neko Neco", sans-serif;
    color: var(--ccPink-bubblegum);
    text-align: center;
    margin: 2em;
    font-size: 50px;
  }

  /* STARS ANIMATION */

  @keyframes scale {
    from,
    to {
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
    --size: clamp(25px, 1.5vw, 30px);
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

  /* BALL PIT */

</style>
