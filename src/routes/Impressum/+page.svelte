<script>
	import Headline from '/src/components/headline.svelte';
    import Logo from "$lib/Logo.png";
</script>


<div class="Seitenende">
   
    <img class="last-picture" src={Logo} alt="Logo" width="200" height="200"/>

    <Headline text="Impressum" />

</div>


<div class="w-full bg-slate-300 h-full text-center">
    <p class="impressum-content">
        <u>Impressum</u><br><br>
        Emelie Rademacher<br>
        Musterstraße 1<br>
        12345 Musterstadt<br>
        Matrikelnummer: 1674349<br>
        Tel.: 01234 567890<br>
        E-Mail: emelie.rademacher@stud.hs-hannover.de<br>
        Web-Adresse: hedwig.wp.hs-hannover.de/home.php</p>
</div>