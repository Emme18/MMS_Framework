<script>
  import Headline from '/src/components/headline.svelte';
  import Logo from "$lib/Logo.png";

  import { onMount } from 'svelte';

  let penguinPosition = 0;

  onMount(() => {
 // ...
 document.addEventListener('keydown', (event) => {
 if (event.key === ' ') {
 penguinPosition -= 50;
 } else if (event.key === 'ArrowUp') {
 const penguin = document.querySelector('.penguin3');
 const bahn3 = document.querySelector('.bahn3');
 const maxTop = parseInt(bahn3.style.top) + 50;
 penguin.style.top = `${Math.max(parseInt(penguin.style.top) - 50, maxTop)}px`;
 } else if (event.key === 'ArrowDown') {
 const penguin = document.querySelector('.penguin3');
 const bahn2 = document.querySelector('.bahn2');
 const minBottom = parseInt(bahn2.style.top) + 50 - 50; // Höhe von bahn2 minus Höhe des Pinguins
 penguin.style.top = `${Math.min(parseInt(penguin.style.top) + 50, minBottom)}px`;
}
});

 document.addEventListener('keyup', (event) => {
 if (event.key === ' ') {
 penguinPosition += 50;
 }
 });

});

onMount(() => {
 const orca = document.querySelector('.orca');
 orca.style.zIndex = 11;
 const bahn3 = document.querySelector('.bahn3');
 const screenWidth = window.innerWidth;
 const screenHeight = window.innerHeight;

 let orcaX = screenWidth;
 let orcaSpeed = 3;

 function moveOrca() {
 orcaX -= orcaSpeed;
 if (orcaX < -screenWidth) {
 orcaX = screenWidth;
 }
 orca.style.left = `${orcaX}px`;
 requestAnimationFrame(moveOrca);
 }

 moveOrca();
});

onMount(() => {
  const achteck = document.querySelector('.achteck');
  achteck.style.position = 'absolute';
  achteck.style.left = '0px';
  achteck.style.top = '10px';
  achteck.style.zIndex = '9';
  const bahn = document.querySelector('.bahn');
  const screenWidth = window.innerWidth;
  const screenHeight = window.innerHeight;

  let achteckX = screenWidth;
  let achteckSpeed = 10;

  function moveAchteck() {
   achteckX -= achteckSpeed;
   if (achteckX < -screenWidth) {
    achteckX = screenWidth;
   }
   achteck.style.left = `${achteckX}px`;
   requestAnimationFrame(moveAchteck);
  }

  moveAchteck();
 });

 onMount(() => {
  const iceberg = document.querySelector('.iceberg');
  iceberg.style.position = 'absolute';
  iceberg.style.top = '-110px'; // Höhe anpassen
  iceberg.style.zIndex = '8';
  const bahn2 = document.querySelector('.bahn2');
  const screenWidth = window.innerWidth;
  const screenHeight = window.innerHeight;

  let icebergX = screenWidth;
  let icebergSpeed = 8;

  function moveIceberg() {
    icebergX -= icebergSpeed;
    if (icebergX < -screenWidth) {
      icebergX = screenWidth;
    }
    iceberg.style.left = `${icebergX}px`;
    requestAnimationFrame(moveIceberg);
  }

  moveIceberg();
});

let isTextfieldOpen = false;

function openTextfield() {
  isTextfieldOpen = true;
}

function closeTextfield() {
  isTextfieldOpen = false;
}

let isOrcaTextfieldOpen = false;

 function openOrcaTextfield() {
 isOrcaTextfieldOpen = true;
 }

 function closeOrcaTextfield() {
 isOrcaTextfieldOpen = false;
 }

 let isAchteckTextfieldOpen = false;

 function openAchteckTextfield() {
  isAchteckTextfieldOpen = true;
 }

 function closeAchteckTextfield() {
  isAchteckTextfieldOpen = false;
 }

 let isInfoTextfieldOpen = false;

function openInfoTextfield() {
isInfoTextfieldOpen = true;
}

function closeInfoTextfield() {
isInfoTextfieldOpen = false;
}
</script>



<div class="Seitenanfang">
  <div><a href="/Charakterwahl"><img class="logo" src={Logo} alt="Logo" width="100" height="100"/></a></div>
  <div><Headline text="Lass den Pinguin nicht verlieren ..." /></div>
  <div> </div>
</div>

<div class="mb-cloud"> 
  <div class="cloud1"></div> 
  <div class="cloud2"></div> 
  <div class="cloud3"></div> 
  <div class="cloud4"></div> 
  <div class="cloud5"></div> 
  <div class="cloud6"></div> 

  <div class="penguin3" style="position: relative; top: {penguinPosition}px; z-index: 10;">
    <div class="penguin-bottom3">
      <div class="right-hand3"></div>
      <div class="left-hand3"></div>
      <div class="right-feet3"></div>
      <div class="left-feet3"></div>
    </div>
    <div class="penguin-top3">
      <div class="right-cheek3"></div>
      <div class="left-cheek3"></div>
      <div class="belly3"></div>
      <div class="right-eye3">
        <div class="sparkle3"></div>
      </div>
      <div class="left-eye3">
        <div class="sparkle3"></div>
      </div>
      <div class="blush-right3"></div>
      <div class="blush-left3"></div>
      <div class="beak-top3"></div>
      <div class="beak-bottom3"></div>
    </div>
  </div>
  
  <div class="track">
    <div class="bahn">
      <div class="achteck" on:click={openAchteckTextfield}>
        <div class="achteck-rechteck"></div>
        <div class="achteck-rechteck"></div>
      </div>
    </div>
    <div class="bahn2" style="top: 45px;">
      <div class="iceberg" on:click={openTextfield}>
        <span></span>
      </div>
    </div>
    <div class="bahn3" style="top: -100px;">
      <div class="orca" on:click={openOrcaTextfield} style="position: absolute; left: 0px;"> <!-- on:mouseover={openOrcaTextfield} ist auch interessant -->
        <div id="orca">     
        <div class="head"></div>
        <div class="spot"></div>
        <div class="front-flipper-perspective">
          <div class="front-flipper"></div>
        </div> 
        <div class="back-flipper-perspective">
         <div class="back-flipper"></div>
        </div>  
        <div class="spine-perspective">
         <div class="spine"></div>
        </div>
        <div class="dorsalfin-perspective">
          <div class="dorsalfin"></div>
        </div>
        <div class="spine-back"></div>       
        <div class="belly"></div>
        <div class="extra"></div>
        <div class="u-b"></div>
        <div class="u-b-t"></div>
        <div class="u-b-w"></div>
        <div class="tail-perspective">
          <div class="tail"></div>
        </div>
      </div>
      </div>
    </div>
   </div>
</div> 
<div class="text-boxes">
  {#if isTextfieldOpen}
  <div class="text-box">
    <p><u>Springen zur Erholung</u><br>
    Der Pinguin ist trotz seiner kurzen Beine ein talentierter Springer. Bis zu 1,80 Meter hoch kann er aus dem Wasser springen. Diese Begabung verwendet der Pinguin unter anderem, um während seiner Tauchgänge Entspannungspausen einzulegen. Dazu springt er auf Eisschollen und andere Eisflächen und verweilt dort, bis die Jagd weitergeht.
    </p>
    <button class="bg-sky-400 hover:bg-sky-600 text-white font-bold py-2 px-4 rounded" on:click={closeTextfield}>Schließen</button>
  </div>
  {/if}
  {#if isAchteckTextfieldOpen}
  <div class="text-box">
  <p><u>Fortbewegung</u><br>
  Der Pinguin ist ein begnadeter Schwimmer. Unter Wasser erreichen einige Arten Geschwindigkeiten von bis zu 30 km/h. Beim Schwimmen dienen die Flügel als Flossen und der Schwanz als Ruder. An Land bewegt sich der Pinguin bekanntermaßen langsam watschelnd voran. Scharfe Krallen sorgen für Haftung am Boden, sodass der Pinguin auf dem Eis nicht ausrutscht. Der Pinguin rutscht auch auf seinem Bauch über das Eis, dann ist er auch an Land schneller unterwegs. 
  </p>
  <button class="bg-sky-400 hover:bg-sky-600 text-white font-bold py-2 px-4 rounded" on:click={closeAchteckTextfield}>Schließen</button>
  </div>
  {/if}
  {#if isOrcaTextfieldOpen}
  <div class="text-box">
  <p><u>Jäger und Gejagter</u><br>
  Der Pinguin ist ein begabter Fischjäger. Zu seiner Beute zählen Fische, Tintenfische und verschiedenste Krebstiere. Wie jedes Lebewesen hat jedoch auch der Pinguin Feinde. Zu diesen zählen vor allem die Seeleoparden, die in Küstennähe jagen. Aber auch Orcas (Schwertwale), Seebären, Seelöwen und Mähnenrobben zählen zu den natürlichen Feinden des Pinguins.
  </p>
  <button class="bg-sky-400 hover:bg-sky-600 text-white font-bold py-2 px-4 rounded" on:click={closeOrcaTextfield}>Schließen</button>
  </div>
  {/if}
</div>

<div class="AllInfo">
  {#if isInfoTextfieldOpen}
  <div class="Info">
  <p class="text-2xl mb-10"><u>Info</u><br>
    Wie sicherlich bereits bemerkt kann der Pinguin nicht verlieren. 😉 <br>
    Dies ist eine animierte Infoseite mit Informationen zum Pinguin. Beim Klick auf die Animationen öffnen sich Kurztexte, deren Quellen sich im Impressum befinden. 
      </p>
  <button class="bg-sky-400 hover:bg-sky-600 text-white font-bold py-2 px-4 rounded text-2xl" on:click={closeInfoTextfield}>Schließen</button>
  </div>
  {/if}
</div>
<button class="bg-sky-400 hover:bg-sky-600 text-white font-bold py-2 px-4 rounded text-2xl" style="position: fixed; bottom: 100px; left: 50%; transform: translateX(-50%);" on:click={openInfoTextfield}>
  Info
</button>

<style>
.penguin-bottom3 .right-feet3, .penguin-bottom3 .left-feet3 {
  animation: walk 2s infinite;
}
</style>