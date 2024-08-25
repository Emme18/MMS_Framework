<script>
	import Button from "../components/button.svelte";
	import Headline from "../components/headline.svelte";
</script>


<h1>Welcome to SvelteKit - über h + enter im Browser öffnen, evtl. nach npm run preview im Terminal </h1>
<p class="bg-green-50 p-4">Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<p>Have fun!</p>

<div class="w-full bg-slate-300 h-full text-center">
    <div class="pt-72">
        <a href="/Spiel_starten">
            <Button />
        </a>

        <Headline text="Überschrift" />
    </div>
</div>





<!-- Diese page.svelte als Willkommenseite definieren, Viel Spaß bei Pingu Run! - ButtonClick und los gehts -->