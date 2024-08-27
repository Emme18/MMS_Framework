<!-- Leer bis notwendig -->

<style>
.cloud1,  
.cloud2,  
.cloud3,  
.cloud4,  
.cloud5,  
.cloud6 {  

  position: relative; /* relative führt zu pinguin und bahnen unten platziert und wolken fliegen über den ganzen bildschirm, fixed wolken nur obere 50% und pinguin und bahnen mittig im Bild */
  width: 100%;
  height: 100%; 

  -webkit-border-radius: 200px;    
  -moz-border-radius: 200px;    
  border-radius: 200px; 
}    
</style>

<script>
onMount(() => {
  const penguin = document.querySelector('.penguin3');
  const orca = document.querySelector('.orca');
 
  function stopAnimation() {
  orca.style.animationPlayState = 'paused';
  }
 
  function checkCollision() {
  const penguinRect = penguin.getBoundingClientRect();
  const orcaRect = orca.getBoundingClientRect();
  if (penguinRect.left < orcaRect.right &&
   penguinRect.right > orcaRect.left &&
   penguinRect.top < orcaRect.bottom &&
   penguinRect.bottom > orcaRect.top) {
  stopAnimation();
  }
  }
 
  function moveOrca() {
  // Animation-Code hier
  checkCollision();
  requestAnimationFrame(moveOrca);
  }
 
  moveOrca();
 });
 </script>