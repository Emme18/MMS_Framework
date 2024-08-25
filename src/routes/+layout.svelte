<script>
    import "../app.css";
    import Logo from "$lib/Logo.png";
</script>
  
  <slot />

  <!-- Inhalte, die hier drin stehen, sind auf jeder Seite zu sehen: Header + Footer, falls sinnvoll für das Spiel -->
  <!-- hilfreich fürs Verlinken https://kit.svelte.dev/docs/link-options -->



  <footer>
	
    <div class="Seitenende">

    <p class="main-footer">
    <u><b>Impressum</b></u><br><br>
    Emelie Rademacher<br>
    Musterstraße 1<br>
    12345 Musterstadt<br>
    <b>Matrikelnummer:</b> 1674349<br>
    <b>Tel.:</b> 01234 567890<br>
    <b>E-Mail:</b> emelie.rademacher@stud.hs-hannover.de<br>
    <b>Web-Adresse:</b> hedwig.wp.hs-hannover.de/home.php</p>

  <!--   <img class="last-picture" src="/Logo.png" alt="Logo" width="200" height="200"> -->
    <img class="last-picture" src={Logo} alt="Logo" width="200" height="200"/>



    </div>
      
    <p class="end-footer"><b>© 2022 Backrezepte</b></p>

  </footer>  

<style>
  /*--Stilistische Elemente des Footers--*/

footer {
	background-color: #004AAD;
	height: 100%;
	margin: 0px auto;
}

.Seitenende {
	display: flex;
	justify-content: space-between;
	background-color: #004AAD;
	padding: 20px;
	margin: auto;
	max-width: 960px;
	font-family: Carter One, sans-serif;
}

.main-footer {
	color: #FFFFFF;
	text-align: left;
	line-height: 15px;
	font-size: 12px;
	padding-top: 20px;
	font-family: Carter One, sans-serif;
}

.last-picture {
	text-align: right;
	order: -1;
}

.end-footer {
	color: #FFFFFF;
	text-align: center;
	font-size: 12px;
	padding-bottom: 5px;
	padding-top: 5px;
	font-family: Carter One, sans-serif;
	border-top: solid 1px #FFFFFF;
}
</style>