<script>
	import Headline from '/src/components/headline.svelte';
    import Logo from "$lib/Logo.png";
</script>



<div class="Seitenanfang">
        <div><a href="/Charakterwahl"><img class="logo" src={Logo} alt="Logo" width="100" height="100"/></a></div>
        <div><Headline text="Impressum" /></div>
        <div> </div>
</div>


<div class="w-full bg-sky-400 h-full text-center">
    <p class="impressum-content">
        <u>Informationen zur Erstellerin:</u><br><br>
        Emelie Rademacher<br>
        Musterstraße 1<br>
        12345 Musterstadt<br>
        Matrikelnummer: 1674349<br>
        Tel.: 01234 567890<br>
        E-Mail: emelie.rademacher@stud.hs-hannover.de<br>
</div>