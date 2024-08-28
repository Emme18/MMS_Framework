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
            <u class="text-2xl">Informationen zur Erstellerin:</u><br><br>
            Emelie Rademacher<br>
            Musterstraße 1<br>
            12345 Musterstadt<br>
            Matrikelnummer: 1674349<br>
            Tel.: 01234 567890<br>
            E-Mail: emelie.rademacher@stud.hs-hannover.de<br></p>
        </div>
        <div>
            <!-- svelte-ignore a11y-missing-attribute -->
            <iframe src="https://giphy.com/embed/nguAwtOo4nxAY" width="240" height="240" style="" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/nguAwtOo4nxAY"></a></p>
        </div>
    </div>
    <div class="Content-Impressum">
        <p>
            <u class="text-2xl">Informationen zur Erstellung des Spiels:</u><br><br>
            Das Spiel "Pingu Run" wurde als Prüfunsleistung der Lehrveranstaltung Multimediasysteme (MM-SYS-2) an der Hochschule Hannover, Studiengang Informationsmanagement (BIM), erstellt. Zusätzlich wurde ein Lerntagebuch als Dokumentation des Vorgehens sowie zur Reflexion verfasst.
            Dieses Tagebuch enthält alle Informationen bezüglich Planung, Quellen und Hilfsmitteln. Im folgenden Teil werden Quellen und Hilfsmittel aufgelistet.
        </p>
    </div>
    <div class="Content-Impressum">
        <p class="text-2xl">Quellen</p>
    </div>
    <div class="Content-Impressum">
            <ul>
                <li>SVG Tastatur - https://commons.wikimedia.org/wiki/File:Tastatur_DE.svg<br> Lizenz: Creative Commons Attribution-Share Alike 4.0 International</li>
                <li>Wolkenanimation - https://www.tnado.com/de/blog/css-animation-und-wolken-beispiele/?cookie=decline</li>
                <li>Pinguine - https://codesandbox.io/p/sandbox/css-animation-penguin-jnjg9v?file=%2Fsrc%2Fstyles.css & https://codepen.io/CyberGirl_/pen/qMmNxe</li>
                <li>Fallende Schneeflocken - https://codepen.io/codeconvey/pen/xRzQay</li>
                <li>GIF-Pinguin - https://giphy.com/gifs/nguAwtOo4nxAY</li>
                <li>Orca - https://codepen.io/ales_codes/pen/LYWZEXX</li>
                <li>Eisberg - https://codepen.io/brycesnyder/pen/OMWGgV</li>
                <li>Text für Orca - https://www.sofatutor.com/sachunterricht/videos/der-pinguin-nahrung-und-feinde</li>
                <li>Text für rutschiges Eis - https://www.wwf-junior.de/tiere/pinguine</li>
                <li>Text für Eisberg - https://www.wwf-junior.de/tiere/pinguine & https://www.spiegel.de/wissenschaft/natur/kaiserpinguine-brauchen-eisflaechen-zur-erholung-bei-der-jagd-a-868694.html</li>
                <li>Logo selbst erstellt über canva.com</li>
            </ul>
    </div>
    <div class="Content-Impressum">
        <p class="text-2xl">Hilfsmittel</p>
    </div>
    <div class="Content-Impressum">
            <ul>
                <li>AcademicCloud</li>
                <li>Google Search</li>
                <li>Svelte - https://svelte.dev/</li>
                <li>Tailwindcss - https://tailwindcss.com/</li>
                <li>W3Schools - https://www.w3schools.com/</li>
                <li>SELFHTML-Wiki - https://wiki.selfhtml.org/wiki/SELFHTML</li>
            </ul>
    </div>
    <div class="Content-Impressum">
        <p><br><br><br><br><br><br></p>  <!-- Platzhalter -->
    </div>
</div>

<style>
    li {
  list-style-type: disc;
}

* {
    color: white;
}
</style>