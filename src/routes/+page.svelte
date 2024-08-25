<script>
	import Button from "../components/button.svelte";
    import Logo from "$lib/Logo.png";
</script>


<div class="flex items-center justify-center h-screen bg-sky-400">
    <div class="Anfang">  
        <img class="last-picture" src={Logo} alt="Logo" width="200" height="200"/>    
        <a href="/Charakterwahl">
            <Button />
        </a>
    </div>  
</div>

<div class="snowflakes" aria-hidden="true">
    <div class="snowflake">
    ❅
    </div>
    <div class="snowflake">
    ❅
    </div>
    <div class="snowflake">
    ❆
    </div>
    <div class="snowflake">
    ❄
    </div>
    <div class="snowflake">
    ❅
    </div>
    <div class="snowflake">
    ❆
    </div>
    <div class="snowflake">
    ❄
    </div>
    <div class="snowflake">
    ❅
    </div>
    <div class="snowflake">
    ❆
    </div>
    <div class="snowflake">
    ❄
    </div>
</div>

<style>

/* customizable snowflake styling */
.snowflake {
  color: #fff;
  font-size: 1em;
  font-family: Arial;
  text-shadow: 0 0 1px #000;
  -webkit-animation-duration: 4s,3s;
  animation-duration: 4s,3s;
}

@-webkit-keyframes snowflakes-fall{0%{top:-10%}100%{top:100%}}
@-webkit-keyframes snowflakes-shake{0%{-webkit-transform:translateX(0px);transform:translateX(0px)}50%{-webkit-transform:translateX(80px);transform:translateX(80px)}100%{-webkit-transform:translateX(0px);transform:translateX(0px)}}
@keyframes snowflakes-fall{0%{top:-10%}100%{top:100%}}@keyframes snowflakes-shake{0%{transform:translateX(0px)}50%{transform:translateX(80px)}100%{transform:translateX(0px)}}.snowflake{position:fixed;top:-10%;z-index:9999;-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none;cursor:default;-webkit-animation-name:snowflakes-fall,snowflakes-shake;-webkit-animation-duration:10s,3s;-webkit-animation-timing-function:linear,ease-in-out;-webkit-animation-iteration-count:infinite,infinite;-webkit-animation-play-state:running,running;animation-name:snowflakes-fall,snowflakes-shake;animation-duration:10s,3s;animation-timing-function:linear,ease-in-out;animation-iteration-count:infinite,infinite;animation-play-state:running,running}.snowflake:nth-of-type(0){left:1%;-webkit-animation-delay:0s,0s;animation-delay:0s,0s}.snowflake:nth-of-type(1){left:10%;-webkit-animation-delay:1s,1s;animation-delay:1s,1s}.snowflake:nth-of-type(2){left:20%;-webkit-animation-delay:6s,.5s;animation-delay:6s,.5s}.snowflake:nth-of-type(3){left:30%;-webkit-animation-delay:4s,2s;animation-delay:4s,2s}.snowflake:nth-of-type(4){left:40%;-webkit-animation-delay:2s,2s;animation-delay:2s,2s}.snowflake:nth-of-type(5){left:50%;-webkit-animation-delay:8s,3s;animation-delay:8s,3s}.snowflake:nth-of-type(6){left:60%;-webkit-animation-delay:6s,2s;animation-delay:6s,2s}.snowflake:nth-of-type(7){left:70%;-webkit-animation-delay:2.5s,1s;animation-delay:2.5s,1s}.snowflake:nth-of-type(8){left:80%;-webkit-animation-delay:1s,0s;animation-delay:1s,0s}.snowflake:nth-of-type(9){left:90%;-webkit-animation-delay:3s,1.5s;animation-delay:3s,1.5s}.snowflake:nth-of-type(10){left:100%;-webkit-animation-delay:2s,0s;animation-delay:2s,0s}.snowflake:nth-of-type(11){left:25%;-webkit-animation-delay:4s,1s;animation-delay:4s,1s}.snowflake:nth-of-type(12){left:75%;-webkit-animation-delay:1s,0.5s;animation-delay:1s,0.5s}.snowflake:nth-of-type(13){left:35%;-webkit-animation-delay:3s,1.5s;animation-delay:3s,1.5s}.snowflake:nth-of-type(14){left:85%;-webkit-animation-delay:2s,1s;animation-delay:2s,1s}.snowflake:nth-of-type(15){left:15%;-webkit-animation-delay:5s,2s;animation-delay:5s,2s}.snowflake:nth-of-type(16){left:45%;-webkit-animation-delay:3s,1s;animation-delay:3s,1s}.snowflake:nth-of-type(17){left:65%;-webkit-animation-delay:2s,0.5s;animation-delay:2s,0.5s}.snowflake:nth-of-type(18){left:95%;-webkit-animation-delay:1s,1.5s;animation-delay:1s,1.5s}.snowflake:nth-of-type(19){left:55%;-webkit-animation-delay:3s,2s;animation-delay:3s,2s}

</style>

<!-- Diese page.svelte als Willkommenseite definieren, Viel Spaß bei Pingu Run! - ButtonClick und los gehts -->