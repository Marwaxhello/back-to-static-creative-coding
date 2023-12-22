<script>

  /* MAGIC SPARKLES */

  import { onMount } from "svelte";

  let stars = [];

  const rand = (min, max) => Math.floor(Math.random() * (max - min + 1)) + min;

  const animate = (star) => {
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
      setTimeout(
        () => {
          animate(star);
          setInterval(() => animate(star), 1000);
        },
        index * (1000 / 3)
      );
    });
  });

  /* BALL PIT */

//  onMount(() => {
//     console.log("Hello World");

//     // Canvas id word aangesproken
//     var canvas = document.getElementById("canvas");
//     //  Hier wordt de 2D-context van het canvas verkregen en toegewezen aan de variabele c. Deze context wordt vaak gebruikt voor het tekenen van grafische elementen op het canvas.
//     var c = canvas.getContext("2d");
//     // Breedte van het canvcas geef je een variabele
//     var tx = window.innerWidth;
//     // Hoogte van het canvas geef je een variabele
//     var ty = window.innerHeight;
//     canvas.width = tx;
//     canvas.height = ty;

//     // Plek van de muis word gevolgd
//     var mousex = 0;
//     var mousey = 0;

//     addEventListener("mousemove", function () {
//       mousex = event.clientX;
//       mousey = event.clientY;
//     });

//     // "zwaartekracht"
//     var grav = 0.99;

//     // Roze kleur word ingesteld
//     function pinkColor() {
//       return "rgba(255, 192, 203, 0.6)"; // Roze kleur met 60% transparantie (0.6)
//     }

//     // Er word een functie aangemaakt voor het ball element
//     function Ball() {
//       // De roze kleur word aangesproken die we eerder hebben ingesteld
//       this.color = pinkColor();
//       // De radius wordt ingesteld op een willekeurige waarde tussen 14 en 34 (20 + 14), waardoor de straal van de bal varieert.
//       this.radius = Math.random() * 20 + 14;
//       // Hier wordt startradius ingesteld op dezelfde waarde als radius op het moment dat hij word aangemaakt. Dit lijkt te worden gebruikt om de oorspronkelijke straal van de bal te onthouden.
//       this.startradius = this.radius;
//       //  De x-positie (this.x) wordt willekeurig ingesteld binnen het canvas, rekening houdend met de grootte van de bal.
//       this.x = Math.random() * (tx - this.radius * 2) + this.radius;
//       // Dit hetzelfde als voor de x-positie
//       this.y = Math.random() * (ty - this.radius);
//       // De dy (delta-y) eigenschap wordt ingesteld op een willekeurige waarde tussen 0 en 2, wat de verticale snelheid van de bal voorstelt.
//       this.dy = Math.random() * 2;
//       //  De dx (delta-x) eigenschap wordt ingesteld op een willekeurige waarde tussen -5 en 5, de horizontale snelheid van de bal.
//       this.dx = Math.round((Math.random() - 0.5) * 10);
//       // De vel (snelheid) eigenschap wordt ingesteld op een willekeurige waarde tussen 0 en 0.2. Dit is de snelheid van de bal.
//       this.vel = Math.random() / 5;
//       // Een methode genaamd update wordt gedefinieerd op het balobject. Deze methode wordt gebruikt om de weergave van de bal bij te werken op basis van zijn huidige eigenschappen.
//       this.update = function () {
//         // Bal word getekend met de waardes die we hierboven hebben ingesteld
//         c.beginPath();
//         c.arc(this.x, this.y, this.radius, 0, 2 * Math.PI);
//         c.fillStyle = this.color;
//         c.fill();
//       };
//     }

//     // Hier wordt een lege array genaamd bal gedeclareerd. Deze array zal worden gebruikt om de balobjecten op te slaan.
//     var bal = [];
//     // Dit is een for-lus die 50 keer wordt doorlopen. De lus heeft een teller i die begint bij 0 en wordt verhoogd met 1 bij elke iteratie. De lus zal doorgaan zolang i kleiner is dan 50.
//     for (var i = 0; i < 50; i++) {
//       // Binnen de lus wordt een nieuwe instantie van het Ball object gemaakt met behulp van de constructorfunctie Ball(). Deze nieuwe instantie wordt vervolgens toegevoegd aan de array bal met behulp van de push-methode
//       bal.push(new Ball());
//     }

//     // Deze functie word gebruikt om een animatie te maken op basis van de eerder gedefinieerde ballen en hun gedrag.
//     function animate() {
//       if (tx != window.innerWidth || ty != window.innerHeight) {
//         tx = window.innerWidth;
//         ty = window.innerHeight;
//         canvas.width = tx;
//         canvas.height = ty;
//       }
//       // Deze blok code controleert of de breedte (tx) of hoogte (ty) van het venster zijn gewijzigd sinds de laatste frame. Als dat het geval is, worden de variabelen tx en ty bijgewerkt met de actuele breedte en hoogte van het venster, en het canvas wordt opnieuw ingesteld op deze nieuwe grootte.

//       // Dit vraagt de browser aan om de functie animate opnieuw aan te roepen voordat de volgende repaint plaatsvindt. Hiermee wordt een soepele animatieloop gemaakt.
//       requestAnimationFrame(animate);
//       // Dit zorgt ervoor dat het canvas aan het begin van elk frame wordt gewist om de oude posities van de ballen te verwijderen voordat de bijgewerkte posities worden getekend.
//       c.clearRect(0, 0, tx, ty);
//       // Deze for-lus itereert over alle ballen in de array bal en voert een reeks bewerkingen uit op elk balobject.
//       for (var i = 0; i < bal.length; i++) {
//         // Dit roept de update-methode aan voor het huidige balobject. Deze methode was eerder gedefinieerd in de Ball constructor en is verantwoordelijk voor het tekenen van de bal op het canvas.
//         bal[i].update();
//         // Hier worden de x- en y-posities van elk balobject bijgewerkt op basis van hun snelheid (dy en dx).
//         bal[i].y += bal[i].dy;
//         bal[i].x += bal[i].dx;
//         // Dit deel controleert of de bal de onderkant van het canvas heeft bereikt. Als dat het geval is, wordt de verticale snelheid (dy) omgekeerd (vermenigvuldigd met -1) en vermenigvuldigd met de zwaartekrachtconstante (grav).
//         if (bal[i].y + bal[i].radius >= ty) {
//           bal[i].dy = -bal[i].dy * grav;
//         }
//         // Als de bal nog niet de onderkant heeft bereikt, wordt de verticale snelheid verhoogd met de snelheid (vel) van de bal.
//         else {
//           bal[i].dy += bal[i].vel;
//         }
//         // Hier wordt gecontroleerd of de bal de rechter- of linkergrens van het canvas heeft bereikt. Als dat het geval is, wordt de horizontale snelheid (dx) omgekeerd (vermenigvuldigd met -1).
//         if (bal[i].x + bal[i].radius > tx || bal[i].x - bal[i].radius < 0) {
//           bal[i].dx = -bal[i].dx;
//         }
//         // Hier wordt gecontroleerd of de muis zich binnen een bepaald gebied rondom een bal bevindt (mousex en mousey worden gebruikt om de muispositie bij te houden). Als dat het geval is en de straal van de bal is kleiner dan 70, wordt de straal van de bal met 5 verhoogd. Anders, als de straal groter is dan de oorspronkelijke straal, wordt de straal met 5 verminderd. Dit creëert een interactie waarbij ballen groter worden als de muis zich in de buurt bevindt, en kleiner als dat niet het geval is.
//         if (
//           mousex > bal[i].x - 20 &&
//           mousex < bal[i].x + 20 &&
//           mousey > bal[i].y - 50 &&
//           mousey < bal[i].y + 50 &&
//           bal[i].radius < 70
//         ) {
//           bal[i].radius += 5;
//         } else {
//           if (bal[i].radius > bal[i].startradius) {
//             bal[i].radius += -5;
//           }
//         }
//       }
//     }

//     animate();
//     //  Deze intervalfunctie voegt elke 400 milliseconden een nieuwe bal toe aan de bal-array en verwijdert tegelijkertijd de oudste bal uit de array. Het resultaat is dat er elke 400 milliseconden een nieuwe bal wordt gecreëerd, en na verloop van tijd zal het aantal ballen in de array constant blijven, omdat er één wordt toegevoegd en één wordt verwijderd.
//     setInterval(function () {
//       // Voegt een nieuwe bal toe aan het einde van de bal-array door een nieuw Ball-object te maken met behulp van de constructorfunctie Ball() en het toe te voegen aan het einde van de array met push.
//       bal.push(new Ball());
//       // Verwijdert het eerste element uit de bal-array (index 0) met behulp van splice. Hierdoor blijft het aantal ballen in de array constant, wat een visueel effect creëert waarbij het lijkt alsof nieuwe ballen continu worden gegenereerd en de oudste ballen verdwijnen.
//       bal.splice(0, 1);
//     }, 400);
//   });

//   export let data;
//   console.log(data);



/* TEST */


</script>

<section>
  <h2>
    <span class="magic">
      <span class="magic-star">
        <svg viewBox="0 0 512 512">
          <path
            d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z"
          />
        </svg>
      </span>

      <span class="magic-star">
        <svg viewBox="0 0 512 512">
          <path
            d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z"
          />
        </svg>
      </span>

      <span class="magic-star">
        <svg viewBox="0 0 512 512">
          <path
            d="M512 255.1c0 11.34-7.406 20.86-18.44 23.64l-171.3 42.78l-42.78 171.1C276.7 504.6 267.2 512 255.9 512s-20.84-7.406-23.62-18.44l-42.66-171.2L18.47 279.6C7.406 276.8 0 267.3 0 255.1c0-11.34 7.406-20.83 18.44-23.61l171.2-42.78l42.78-171.1C235.2 7.406 244.7 0 256 0s20.84 7.406 23.62 18.44l42.78 171.2l171.2 42.78C504.6 235.2 512 244.6 512 255.1z"
          />
        </svg>
      </span>
      <span class="magic-text">Bubblegum Kennisclips</span>
    </span>
  </h2>

   <canvas id="c"></canvas>
<div id="info">
  <a id="close" href="">
  &#215;
  </a>
  <div class="title">
  Ball Physics
  </div>
  <div class="item">
  &#8226; Right click to interact.
  </div>
  <div class="item">
  &#8226; Left click to add a new ball.
  </div>
</div>

</section>

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
