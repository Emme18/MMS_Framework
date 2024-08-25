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

<!-- Diese page.svelte als Willkommenseite definieren, Viel Spaß bei Pingu Run! - ButtonClick und los gehts -->