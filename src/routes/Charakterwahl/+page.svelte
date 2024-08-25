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
    <div><Headline text="Spiel starten" /></div>
    <div> </div>
</div>

<div class="Charakter">
    <h1 class="w-full my-10 py-10 text-3xl text-center">Wähle Deinen Pinguin</h1>
</div>

<div class="Pinguine">
    <div class="penguin">
    <div class="penguin-head">
        <div class="face left"></div>
        <div class="face right"></div>
        <div class="chin"></div>
        <div class="eye left">
        <div class="eye-lid"></div>
        </div>
        <div class="eye right">
        <div class="eye-lid"></div>
        </div>
        <div class="blush left"></div>
        <div class="blush right"></div>
        <div class="beak top"></div>
        <div class="beak bottom"></div>
    </div>
    <div class="penguin-body">
        <div class="arm left"></div>
        <div class="arm right"></div>
        <div class="foot left"></div>
        <div class="foot right"></div>
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

      <div class="penguin_container3">
		<div class="body3">
			<div class="wings3">
				<span></span>
				<span></span>
			</div>

			<div class="face_container3">
				<div class="face_white3">
					<span></span>
					<span></span>
				</div>

				<div class="eyes3">
					<span></span>
					<span></span>
				</div>

				<div class="beak3">
					<span></span>
					<span></span>
				</div>

				<div class="cheeks3">
					<span></span>
					<span></span>
				</div>
			</div>
			
			<div class="belly3"></div>

			<div class="feet3">
				<span></span>
				<span></span>
			</div>
      
		</div>
      </div>      
</div>

<style>


.penguin_container3 {
  margin: 0 auto;
  position: absolute;
  left: 0;
  right: 0;
  width: 333px;
  top: 15%;
}

.body3 {
	width: 298px;
	height: 333px;
	border-top-left-radius: 45%;
  border-top-right-radius: 45%;
  border-bottom-left-radius: 35%;
  border-bottom-right-radius: 35%;
	background: #465a65;
	position: absolute;
}

/* belly */

.belly3 {
  width: 240px;
  background: #deddd0;
  border-bottom-left-radius: 50%;
  border-bottom-right-radius: 50%;
  height: 150px;
  margin: 0 auto;
  margin-top: 150px;
  overflow: hidden;
}

.belly3::before {
  content: '';
  width: 240px;
  background: #f6f5e4;
  border-bottom-left-radius: 55%;
  border-bottom-right-radius: 43%;
  height: 135px;
  display: block;
  position: absolute;
}

/* face white */

.face_white3 span {
  height: 100px;
  background: #f6f5e4;
  width: 121px;
  position: absolute;
  top: 55px;
}

.face_white3 span:nth-child(1) {
  left: 29px;
  border-top-left-radius: 100%;
  border-top-right-radius: 50%;
}

.face_white3 span:nth-child(2) {
	right: 29px;
  border-top-right-radius: 100%;
  border-top-left-radius: 50%;
}


/* eyes */

.eyes3 span {
  width: 40px;
  height: 40px;
  background: #263238;
  border-radius: 50%;
  position: absolute;
  top: 100px;
}

.eyes3 span:nth-child(1) {left: 70px;}

.eyes3 span:nth-child(2) {right: 70px;}

.eyes3 span::after {
  content: '';
  position: absolute;
  background: #fff;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  top: 8px;
  left: 9px;
}

/* beak */

.beak3 span:nth-child(1) {
  width: 35px;
  height: 35px;
  background: #f5b81f;
  position: absolute;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
  left: 130px;
  top: 130px;
  z-index: 9;
  border-radius: 15%;
}

.beak3 span:nth-child(2) {
  width: 50px;
  height: 10px;
  border-bottom: 5px solid #262626;
  position: absolute;
  top: 138px;
  left: 123px;
  z-index: 999;
  border-radius: 50%;
}

/* cheeks */

.cheeks3 span {
  width: 30px;
  height: 15px;
  border-radius: 50%;
  background: pink;
  position: absolute;
  top: 145px;
  z-index: 99;
}

.cheeks3 span:nth-child(1) {
	left: 54px;
}

.cheeks3 span:nth-child(2) {
	right: 54px;
}

/* feet */

.feet3 span {
  width: 40px;
  height: 90px;
  position: absolute;
  background: #f5b81f;
  border-radius: 50%;
  bottom: -42px;
  z-index: -1;
}

.feet3 span:nth-child(1) {
  -webkit-transform: rotate(77deg);
  -ms-transform: rotate(77deg);
	transform: rotate(77deg);
  left: 60px;
}

.feet3 span:nth-child(2) {
  -webkit-transform: rotate(-77deg);
  -ms-transform: rotate(-77deg);
  transform: rotate(-77deg);
  right: 60px;	
}


/* wings */

.wings3 span {
  width: 35px;
  height: 90px;
  position: absolute;
  background: #334852;
  border-radius: 50%;
  top: 136px;
  z-index: -1;
}

.wings3 span:nth-child(1) {
  left: -30px;
  -webkit-transform: rotate(140deg);
  -ms-transform: rotate(140deg);
  transform: rotate(140deg);
  border-bottom-left-radius: 100%;
}

.wings3 span:nth-child(2) {
  right: -30px;
  -webkit-transform: rotate(-140deg);
  -ms-transform: rotate(-140deg);
  transform: rotate(-140deg);
  border-bottom-right-radius: 100%;
}



</style>