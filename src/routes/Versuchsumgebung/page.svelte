<script>
    import Headline from '/src/components/headline.svelte';
    import Logo from "$lib/Logo.png";
   
    import { onMount } from 'svelte';
   
    let penguinPosition = 0;
    let penguinPositionX = 0;
   
    onMount(() => {
    document.addEventListener('keydown', (event) => {
    if (event.key === ' ') {
    penguinPosition -= 30;
    }
    });
   
    document.addEventListener('keyup', (event) => {
    if (event.key === ' ') {
    penguinPosition += 30;
    }
    });
   
    document.addEventListener('keydown', (event) => {
    if (event.key === 'ArrowRight') {
    penguinPositionX += 10;
    }
    });
   
    document.addEventListener('keydown', (event) => {
    if (event.key === 'ArrowLeft') {
    penguinPositionX -= 10;
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
  </div> 
  
  <div class="penguin3" style="position: relative; left: {penguinPositionX}px; top: {penguinPosition}px;">
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
