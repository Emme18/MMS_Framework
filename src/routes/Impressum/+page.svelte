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
    <div class="Content-Impressum">
        <div>
            <p class="impressum-content">
            <u>Informationen zur Erstellerin:</u><br><br>
            Emelie Rademacher<br>
            Musterstraße 1<br>
            12345 Musterstadt<br>
            Matrikelnummer: 1674349<br>
            Tel.: 01234 567890<br>
            E-Mail: emelie.rademacher@stud.hs-hannover.de<br></p>
        </div>
        <div>
            <iframe src="https://giphy.com/embed/nguAwtOo4nxAY" width="240" height="240" style="" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/nguAwtOo4nxAY"></a></p>
        </div>
    </div>
    <div class="Content-Impressum">
        <p>
            <u>Informationen zur Erstellung des Spiels:</u><br><br>
            Das Spiel "Pingu Run" wurde als Prüfunsleistung der Lehrveranstaltung Multimediasysteme (MM-SYS-2) an der Hochschule Hannover, Studiengang Informationsmanagement (BIM), erstellt. Zusätzlich wurde ein Lerntagebuch als Dokumentation des Vorgehens sowie zur Reflexion verfasst.
            Dieses Tagebuch enthält alle Informationen bezüglich Planung, Quellen und Hilfsmitteln. Im folgenden Teil werden Quellen und Hilfsmittel aufgelistet.
        </p>
    </div>
    <div class="Content-Impressum">
            <ul>
                <li>eine Spalte mit Quellen</li>
                <li>eine Spalte mit Hilfsmitteln</li>
            </ul>
    </div>
</div>