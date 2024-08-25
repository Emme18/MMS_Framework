<script>
	import Headline from '/src/components/headline.svelte';
    import Logo from "$lib/Logo.png";
</script>

<!-- sinnvoll: hier den eigentlichen Spielinhalt verbauen
 Hauptseite (Index) von routes als Idle Screen, "wähle deinen Pinguin"
 Preloader/Animation als Übergang zum Spiel (hier)
 Redirect, wenn die Runde verloren wurde, damit wieder im Idle Screen gelandet wird
 AUCH sinnvoll sind Unterseiten wie Credits oder Anleitung -->


 <div class="Seitenanfang">
    <div><a href="/Charakterwahl"><img class="logo" src={Logo} alt="Logo" width="100" height="100"/></a></div>
    <div><Headline text="Charakterwahl" /></div>
    <div> </div>
</div>


 <p> Test </p>