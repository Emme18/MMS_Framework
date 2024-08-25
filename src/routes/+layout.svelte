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
    <u>Impressum</u><br><br>
    Emelie Rademacher<br>
    Musterstraße 1<br>
    12345 Musterstadt<br>
    Matrikelnummer: 1674349<br>
    Tel.: 01234 567890<br>
    E-Mail: emelie.rademacher@stud.hs-hannover.de<br>
    Web-Adresse: hedwig.wp.hs-hannover.de/home.php</p>

  <!--   <img class="last-picture" src="/Logo.png" alt="Logo" width="200" height="200"> -->
    <img class="last-picture" src={Logo} alt="Logo" width="200" height="200"/>



    </div>
      
    <p class="end-footer">© 2024 Pingu Run</p>

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
	font-family: Carter One, sans-serif;
  position: sticky; 
  bottom: 0; 
  left: 0; 
  width: 100%; 
  margin: 0;
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
  position: sticky; 
  bottom: 0; 
  left: 0; 
  width: 100%; 
  margin: 0;
}
</style>