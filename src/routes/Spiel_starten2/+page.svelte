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
   const penguin = document.querySelector('.penguin2');
   const bahn3 = document.querySelector('.bahn3');
   const maxTop = parseInt(bahn3.style.top) + 50;
   penguin.style.top = `${Math.max(parseInt(penguin.style.top) - 50, maxTop)}px`;
   } else if (event.key === 'ArrowDown') {
   const penguin = document.querySelector('.penguin2');
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
   orca.style.zIndex = 10;
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
  
    <div class="penguin2" style="position: relative; top: {penguinPosition}px; z-index: 1;">
      <div class="penguin-bottom2">
        <div class="right-hand2"></div>
        <div class="left-hand2"></div>
        <div class="right-feet2"></div>
        <div class="left-feet2"></div>
      </div>
      <div class="penguin-top2">
        <div class="right-cheek2"></div>
        <div class="left-cheek2"></div>
        <div class="belly2"></div>
        <div class="right-eye2">
          <div class="sparkle2"></div>
        </div>
        <div class="left-eye2">
          <div class="sparkle2"></div>
        </div>
        <div class="blush-right2"></div>
        <div class="blush-left2"></div>
        <div class="beak-top2"></div>
        <div class="beak-bottom2"></div>
      </div>
    </div>
    
    <div class="track">
      <div class="bahn">
        <div class="achteck">
          <div class="achteck-rechteck"></div>
          <div class="achteck-rechteck"></div>
        </div>
      </div>
      <div class="bahn2" style="top: 45px;">
        <div class="iceberg">
          <span></span>
        </div>
      </div>
      <div class="bahn3" style="top: -100px;">
        <div class="orca" style="position: absolute; left: 0px;">
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
  
  <style>
    .penguin-bottom2 .right-feet2, .penguin-bottom2 .left-feet2 {
      animation: walk 2s infinite;
    }
    </style>