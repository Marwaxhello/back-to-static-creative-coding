<script>
  
</script>

<main>
  <h1>post apocalyptic thinking</h1>
  <p>
    After the apocalypse, cities crumbled into silence. Dust-choked winds
    whisper through skeletal skyscrapers, and the sky weeps in hues of blood and
    ash. Survivors, faces etched with fear, scavenge a world that no longer
    recognizes mercy. A once-vibrant civilization is now reduced to shadows and
    ruins. The future is uncertain, a tapestry woven with threads of decay and
    despair. Amidst the darkness, resilient hearts endure, seeking a glimmer of
    hope in the unforgiving aftermath. In the ruins, the echoes of the past may
    guide survivors toward an uncertain tomorrow.
  </p>

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

    <img src="./bloody-handprint-4.png" alt="bloody handprint" loading="lazy" />
  </section>
</main>

<style>
  @import url("https://fonts.cdnfonts.com/css/apocalypse");

  h1 {
    font-family: "Apocalypse", sans-serif;
    font-size: 7em;
    color: #b00808;
    position: absolute;
    left: 1em;
    margin-top: 2em;
    z-index: 999; /* Ensure the h1 is on top */
    animation:
      fallHard 2s cubic-bezier(0.4, 0, 0.2, 1),
      fall 5s ease-in-out; /* Combine both animations */
    text-align: left;
  }

  p {
    font-family: "Apocalypse", sans-serif;
    font-size: 1.3em;
    color: white;
    position: absolute;
    z-index: 999; /* Ensure the h1 is on top */
    text-align: left;
    width: 50%; /* Adjust the width as needed */
    top: 45%;
    left: 31.5%;
    transform: translateX(-50%);
    opacity: 50%;
  }

  img {
    position: absolute;
    top: 40%;
    left: 60%;
    z-index: 1000;
    rotate: 9deg;
    animation: glitch 4s linear infinite;
    width: 400px;
    height: 450px;
  }

  /* Keyframes */
  @keyframes fallHard {
    0% {
      transform: translateY(-100vh);
    }

    50% {
      transform: translateY(-25vh);
      opacity: 1;
    }

    25%,
    55%,
    75%,
    87%,
    97%,
    100% {
      transform: translateY(0);
    }
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

  @keyframes glitch {
    2%,
    64% {
      transform: translate(2px, 0) skew(0deg);
    }
    4%,
    60% {
      transform: translate(-2px, 0) skew(0deg);
    }
    62% {
      transform: translate(0, 0) skew(5deg);
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

  /* Media Queries Tablet */
  @media only screen and (min-width: 601px) and (max-width: 1024px) {
    h1 {
      font-size: 4em;
      left: 1.4em;
      top:20%;
      
    }

    p {
      font-size: 1.2em;
      width: 80%;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }

    img {
      top: 55%;
      left: 65%;
      transform: translateX(-50%);
      width: 300px;
      height: 350px;
    }
  }

  /* Media Queries Mobile */
  @media (max-width: 600px) {
    h1 {
      font-size: 3em;
      left: 0.7em;
      right: 1em;
      margin-right: 2em;
      top:30%;
    }

    p {
      font-size: 0.8em;
      width: 78%;
      top: 45%;
      margin-left: 4.5em;
      right: 1em;
    }

    img {
      top: 58%;
      width: 200px;
      height: 250px;
    }
  }
</style>
