<script>
	import Button from "../components/button.svelte";
    import Logo from "$lib/Logo.png";
</script>


<div class="flex items-center justify-center h-screen bg-sky-400">
    <div class="Anfang">  
        <img class="logo" src={Logo} alt="Logo" width="200" height="200"/>    
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