<script></script>

<main>
  <h1>post apocalyptic soul lake</h1>

  <section class="waveWrapper waveAnimation">
    <article class="waveWrapperInner bgTop">
      <aside
        class="wave waveTop"
        style="background-image: url('http://front-end-noobs.com/jecko/img/wave-top.png')"
      ></aside>
    </article>

    <article class="waveWrapperInner bgMiddle">
      <aside
        class="wave waveMiddle"
        style="background-image: url('http://front-end-noobs.com/jecko/img/wave-mid.png')"
      ></aside>
    </article>

    <article class="waveWrapperInner bgBottom">
      <aside
        class="wave waveBottom"
        style="background-image: url('http://front-end-noobs.com/jecko/img/wave-bot.png')"
      ></aside>
    </article>

    <img
      src="./bloody-handprint-4.png"
      alt="bloody handprint"
      style="width: 100px; height: 100px;"
      loading="lazy"
    />
  </section>

</main>

<style>
  @import url("https://fonts.cdnfonts.com/css/apocalypse");

  h1 {
    font-family: "Apocalypse", sans-serif;
    font-size: 5em;
    color: #b00808;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 999; /* Ensure the h1 is on top */
  }

  @keyframes move_wave {
    0% {
      transform: translateX(0) translateZ(0) scaleY(1);
    }
    50% {
      transform: translateX(-25%) translateZ(0) scaleY(0.55);
    }
    100% {
      transform: translateX(-50%) translateZ(0) scaleY(1);
    }
  }

  .waveWrapper {
    overflow: hidden;
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
    margin: auto;
  }
  .waveWrapperInner {
    position: absolute;
    width: 100%;
    overflow: hidden;
    height: 100%;
    bottom: -1px;
    background-image: linear-gradient(to top, #260606 20%, #1a1a28 80%);
  }
  .bgTop {
    z-index: 15;
    opacity: 0.5;
  }
  .bgMiddle {
    z-index: 10;
    opacity: 0.75;
  }
  .bgBottom {
    z-index: 5;
  }
  .wave {
    position: absolute;
    left: 0;
    width: 200%;
    height: 100%;
    background-repeat: repeat no-repeat;
    background-position: 0 bottom;
    transform-origin: center bottom;
  }
  .waveTop {
    background-size: 50% 100px;
  }
  .waveAnimation .waveTop {
    animation: move-wave 3s;
    -webkit-animation: move-wave 3s;
    -webkit-animation-delay: 1s;
    animation-delay: 1s;
  }
  .waveMiddle {
    background-size: 50% 120px;
  }
  .waveAnimation .waveMiddle {
    animation: move_wave 10s linear infinite;
  }
  .waveBottom {
    background-size: 50% 100px;
  }
  .waveAnimation .waveBottom {
    animation: move_wave 15s linear infinite;
  }

  img {
    position: absolute;
    width: 100px;
    height: 100px;
    top: 50%;
    left: 90%;
    z-index: 1000; /* Set a higher z-index to make sure it's above the waves */
    /* Additional styling if needed */
    rotate: 10deg;
    
  }

  img {
    position: absolute;
    width: 50%; /* Responsive width */
    height: auto; /* Maintain aspect ratio */
    max-width: 600px; /* Limit maximum width */
    top: 50%;
    left: 20%;
    z-index: 1000;
    /* Set a higher z-index to make sure it's above the waves */
    /* Additional styling if needed */
    rotate: 10deg;
  }

  /* Responsive Font Size for Mobile */
  @media screen and (max-width: 480px) {
    h1 {
      font-size: 3em;
    }
    img {
      top: 60%;
      left: 10%;
      margin: 0;
    }
  }

  /* Responsive Font Size for Tablet */
  @media screen and (min-width: 481px) and (max-width: 820px) {
    h1 {
      font-size: 4em;
    }
    img {
      top: 60%;
      left: 20%;
      margin: 0;
    }
  }
</style>
