<script>
	import Headline from '/src/components/headline.svelte';
    import Logo from "$lib/Logo.png";

    import Tastatur from '$lib/Tastatur.svg';

    let showTastatur = false;

    function toggleTastatur(event) {
    if (event.key === 'Escape') {
    showTastatur = false;
    } else {
    showTastatur = !showTastatur;
    }
    };

    document.addEventListener('keydown', toggleTastatur);

    import { onMount } from 'svelte';

    let pinguinElement;

    onMount(() => {
        pinguinElement = document.querySelector('.penguin');

        pinguinElement.addEventListener('click', () => {
        // Öffne die Seite mit dem Namen "Spiel_starten"
        window.location.href = '/Spiel_starten';
        });
    });
    onMount(() => {
        pinguinElement = document.querySelector('.penguin2');

        pinguinElement.addEventListener('click', () => {
        // Öffne die Seite mit dem Namen "Spiel_starten2"
        window.location.href = '/Spiel_starten2';
        });
    });
    onMount(() => {
        pinguinElement = document.querySelector('.penguin3');

        pinguinElement.addEventListener('click', () => {
        // Öffne die Seite mit dem Namen "Spiel_starten3"
        window.location.href = '/Spiel_starten3';
        });
    });
</script>

<!--Redirect, wenn die Runde verloren wurde, damit wieder im Idle Screen gelandet wird -->


<div class="Seitenanfang">
    <div><a href="/Charakterwahl"><img class="logo" src={Logo} alt="Logo" width="100" height="100"/></a></div>
    <div><Headline text="Spiel starten" /></div>
    <div> </div>
</div>

<button style="background-color: #004AAD; 
font-family: Carter One, sans-serif; 
font-size: 30px;" class="p-4 text-white" on:click={toggleTastatur}>Anleitung</button>

{#if showTastatur}
 <div class="fixed top-0 left-0 w-1/2 h-1/2 bg-white overflow-hidden z-10" />
 <div class="fixed top-20 left-0 w-1/2 h-1/2 overflow-hidden z-10 order-1">
 <img src={Tastatur} alt="Tastatur" class="w-full h-full object-cover" />
 </div>
{/if}

<div class="Schrift-Wahl">
    <h1 class="w-full my-10 py-10 text-3xl text-center">Wähle Deinen Pinguin</h1>
</div>

<div class="Pinguine">
    <div class="penguin">
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

    <div class="penguin2">
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

      <div class="penguin3">
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
            <div class="eye-lid3"></div>
        </div>
          <div class="blush-right3"></div>
          <div class="blush-left3"></div>
          <div class="beak-top3"></div>
          <div class="beak-bottom3"></div>
        </div>
      </div>        
</div>