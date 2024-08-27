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
 const penguin = document.querySelector('.penguin');
 const bahn3 = document.querySelector('.bahn3');
 const maxTop = parseInt(bahn3.style.top) + 50;
 penguin.style.top = `${Math.max(parseInt(penguin.style.top) - 50, maxTop)}px`;
 } else if (event.key === 'ArrowDown') {
 const penguin = document.querySelector('.penguin');
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
 let orcaSpeed = 4;

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
  let achteckSpeed = 3;

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
  let icebergSpeed = 2;

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

  <div class="penguin" style="position: relative; top: {penguinPosition}px; z-index: 10;">
    <div class="penguin-bottom">
      <div class="right-hand"></div>
      <div class="left-hand"></div>
      <div class="right-feet"></div>
      <div class="left-feet"></div>
    </div>
    <div class="penguin-top">
      <div class="right-cheek"></div>
      <div class="left-cheek"></div>
      <div class="belly"></div>
      <div class="right-eye">
        <div class="eye-lid"></div>
      </div>
      <div class="left-eye">
        <div class="eye-lid"></div>
      </div>
      <div class="blush-right"></div>
      <div class="blush-left"></div>
      <div class="beak-top"></div>
      <div class="beak-bottom"></div>
    </div>
  </div>
  
  <div class="track">
    <div class="bahn">
      <div class="achteck" on:click={openAchteckTextfield}>
        <div class="achteck-rechteck"></div>
        <div class="achteck-rechteck"></div>
      </div>
      {#if isAchteckTextfieldOpen}
      <div class="absolute top-10 left-10 bg-white p-4">
      <p>Achteck-Textfeld ist offen!</p>
      <button on:click={closeAchteckTextfield}>Schließen</button>
      </div>
      {/if}
    </div>
    <div class="bahn2" style="top: 45px;">
      <div class="iceberg" on:click={openTextfield}>
        <span></span>
      </div>
      {#if isTextfieldOpen}
      <div class="textfield absolute top-10 left-10 bg-white p-4">
        <p>Textfeld ist offen! - Funktioniert</p>
        <button on:click={closeTextfield}>Schließen</button>
      </div>
      {/if}
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
      {#if isOrcaTextfieldOpen}
      <div class="absolute top-10 left-10 bg-white p-4">
      <p>Orca-Textfeld ist offen!</p>
      <button on:click={closeOrcaTextfield}>Schließen</button>
      </div>
      {/if}
    </div>
   </div>
</div> 

<style>
.penguin-bottom .right-feet, .penguin-bottom .left-feet {
  animation: walk 2s infinite;
}

.orca:hover, .iceberg:hover, .achteck:hover {
  /* Hier kannst du die Anzeigeform ändern */
  cursor: pointer;
  transform: scale(1.1);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}
</style>
