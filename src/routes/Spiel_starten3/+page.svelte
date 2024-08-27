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

  <div class="penguin3" style="position: relative; top: {penguinPosition}px; z-index: 1;">
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
    <div class="bahn"></div>
    <div class="bahn2" style="top: 45px;"></div>
    <div class="bahn3" style="top: -100px;"></div>
   </div>
</div> 

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

<style>
  :root {
    --color-dark: rgb(1, 2, 17);
    --color-light: rgb(255, 255, 255);
}

/* orca */

#orca {        
    width: 0px;
    position: relative;       
    transform: scale(.2) rotateY(180deg);  
    position: relative;
    margin: auto;
    display: block;   
}

.head {    
    width: 420px;
    height: 209px;
    border-radius: 50%;    
    background-color: var(--color-light);
    border-top: 85px solid var(--color-dark);    
    border-right: 3px solid var(--color-dark);        
}

.spot {
    width: 150px;
    height: 35px;
    background-color: var(--color-light);
    top: 15px;
    position: absolute;
    left: 120px;
    border-top-left-radius: 30%;
    border-top-right-radius: 60%;
    border-bottom-left-radius: 60%;
    border-bottom-right-radius: 60%;
    z-index: 0;
}

/* flipper front */ 

.front-flipper-perspective {
    perspective: 120px;
    perspective-origin: right; 
    position: absolute;
    top: 10px;
    left: -10px;
}
.front-flipper {
    width: 120px;
    height: 210px;
    background-color: var(--color-dark);
    border-radius: 20% 20% 60% 20%;   
    transform: rotateX(40deg);    
}

/* flipper back */ 
.back-flipper-perspective {
    perspective: 120px;
    perspective-origin: left;    
    position: absolute;
    top: 140px;
    left: 130px;  
    z-index: -1;     
}

.back-flipper {
    width: 100px;
    height: 140px;
    background-color: var(--color-dark);    
    border-radius: 22% 10% 50% 20%;    
    transform: rotateX(20deg);
    position: relative;
}

.back-flipper:before {
    content: '';
    width: 180px;
    height: 15px;
    border-radius: 90%;
    border-bottom: 1px solid var(--color-dark);
    position: absolute;
    left: -30px;
    top: 51px;
    transform: rotateZ(3deg);
}

/* spine 1 */
.spine-perspective {    
    perspective: 100;
    position: absolute;
    top: -27px;
    left: 0px;    
}

.spine {
    width: 370px;
    height: 55px;
    background-color: var(--color-dark);    
    border-radius: 100% 100% 0 0;
    transform: rotateZ(12deg);
}


/* spine 2 */
.spine-back {
    width: 940px;
    height: 600px;    
    border-radius: 100%;
    border-top: 125px solid var(--color-dark);
    border-right: 120px solid transparent;
    z-index: -1;
    position: absolute;
    left: -600px;
    top: -30px;
    transform: rotateZ(-20deg);
}

/* dorsal fin */
.dorsalfin-perspective {
    perspective: 180px;
    perspective-origin: left;
    position: absolute;
    top: -290px;
    left: -120px;
    transform: rotateZ(-10deg);
}

.dorsalfin {
    width: 85px;
    height: 290px;
    background-color: var(--color-dark);        
    transform: rotateX(40deg);
    border-top-right-radius: 90%;
    border-top-left-radius: 10px;
}

/* belly */
.belly {
    width: 710px;
    height: 510px;    
    border-top: 120px solid var(--color-light);
    border-right: 60px solid transparent;
    border-left: 10px solid transparent;
    border-radius: 90%;    
    position: absolute;
    top: 122px;
    left: -570px;
    transform: rotateZ(-20deg);
    z-index: -1;
    display: none;
}

.extra {
    width: 300px;
    height: 100px;
    background-color: var(--color-light);    
    position: absolute;
    top: 105px;
    left: -170px;
    z-index: -1;
}

.extra::after {
    content: '';
    width: 360px;
    height: 80px;
    border-top: 2px solid var(--color-dark);
    border-right: 4px solid transparent;
    border-top-left-radius: 30%;
    position: absolute;    
    top: 106px;
    left: -55px;
    z-index: -1;
    transform: rotateZ(-3deg);
}

.u-b {
    width: 500px;
    height: 140px;
    background-color: var(--color-dark);
    border-radius: 90%;
    left: -440px;
    top: 60px;
    position: absolute;
    transform: rotateZ(-18deg);
}

.u-b-t {
    width: 300px;
    height: 150px;    
    border-top: 45px solid var(--color-dark);
    border-radius: 46%;
    left: -564px;
    top: 290px;
    position: absolute;    
    transform: rotateZ(-36deg);
    z-index: -1;
    background-color: transparent;
} 

.u-b-w {
    position: absolute;
    width: 400px;
    height: 280px;
    border-top: 80px solid var(--color-light);
    transform: rotateZ(-30deg);
    border-radius: 80%;
    left: -588px;
    top: 200px;
}

/* Tail */
.tail-perspective {
    perspective: 180px;  
    position: absolute;
    top: 445px;
    left: -642px;     
    transform: rotateZ(3deg);
}

.tail {
    width: 260px;
    height: 150px;
    transform: rotateY(30deg); 
    border-top: 50px solid var(--color-dark);
    border-radius: 60%;    
}

.tail::after {
    content: '';
    width: 0px;
    height: 0px;    
    border-style: solid;
    border-width: 20px;
    border-color: transparent var(--color-dark) var(--color-dark) var(--color-dark);
    position: absolute;  
    top: -70px;  
    left: 60px;
}
</style>



