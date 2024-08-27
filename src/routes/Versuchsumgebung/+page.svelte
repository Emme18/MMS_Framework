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

 const orca = document.querySelector('.orca');
 const achteck = document.querySelector('.achteck');
 const iceberg = document.querySelector('.iceberg');

 let orcaMoving = true;
 let achteckMoving = true;
 let icebergMoving = true;

 document.addEventListener('keydown', (event) => {
 if (event.key === 'Enter') {
 orcaMoving = false;
 achteckMoving = false;
 icebergMoving = false;
 }
 });

 document.addEventListener('keyup', (event) => {
 if (event.key === 'Enter') {
 orcaMoving = true;
 achteckMoving = true;
 icebergMoving = true;
 }
 });

 function moveOrca() {
 if (orcaMoving) {
 const orca = document.querySelector('.orca');
 const orcaX = parseInt(orca.style.left);
 const screenWidth = window.innerWidth;
 orca.style.left = `${orcaX - 4}px`;
 if (orcaX < -screenWidth) {
 orca.style.left = `${screenWidth}px`;
 }
 requestAnimationFrame(moveOrca);
 }
 }

 function moveAchteck() {
 if (achteckMoving) {
 const achteck = document.querySelector('.achteck');
 const achteckX = parseInt(achteck.style.left);
 const screenWidth = window.innerWidth;
 achteck.style.left = `${achteckX - 3}px`;
 if (achteckX < -screenWidth) {
 achteck.style.left = `${screenWidth}px`;
 }
 requestAnimationFrame(moveAchteck);
 }
 }

 function moveIceberg() {
 if (icebergMoving) {
 const iceberg = document.querySelector('.iceberg');
 const icebergX = parseInt(iceberg.style.left);
 const screenWidth = window.innerWidth;
 iceberg.style.left = `${icebergX - 2}px`;
 if (icebergX < -screenWidth) {
 iceberg.style.left = `${screenWidth}px`;
 }
 requestAnimationFrame(moveIceberg);
 }
 }

 var orcaInterval = setInterval(moveOrca, 16);
 var achteckInterval = setInterval(moveAchteck, 16);
 var icebergInterval = setInterval(moveIceberg, 16);

 document.addEventListener('keydown', (event) => {
 if (event.key === 'Enter') {
 clearInterval(orcaInterval);
 clearInterval(achteckInterval);
 clearInterval(icebergInterval);
 }
 });

 document.addEventListener('keyup', (event) => {
 if (event.key === 'Enter') {
 orcaInterval = setInterval(moveOrca, 16);
 achteckInterval = setInterval(moveAchteck, 16);
 icebergInterval = setInterval(moveIceberg, 16);
 }
 });
});

</script>

<!-- Funktioniert nicht wie gewollt, nur der Orca bewegt sich noch und reagiert auf Enter als Stop -->