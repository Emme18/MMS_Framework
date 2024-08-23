<script>
	import Button from "../components/button.svelte";
	import Headline from "../components/headline.svelte";

    import { onMount } from 'svelte';

    let contents = [];

    onMount(async () => {
        const response = await fetch("https://api.sampleapis.com/coffee/hot");

        if (response.ok) {
            const data = await response.json();
            contents = data;
        } else {
            console.error("Failed to fetch data:", response.status.Text);
        }
    });
    
</script>


<h1>Welcome to SvelteKit - über h + enter im Browser öffnen, evtl. nach npm run preview im Terminal </h1>
<p class="bg-green-50 p-4">Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<p>Have fun!</p>

<div class="w-full bg-slate-300 h-full text-center">
    <div class="pt-72">
        <a href="/Charakterwahl">
            <Button />
        </a>

        <Headline text="Überschrift" />
    </div>

    <div class="md:flex-wrap md:flex flex-row w-2/3 m-auto text-center justify-center gap-4 py-20 px-16">
        {#each contents as content} 
        <div class="bg-lime-400 rounded-lg p-8"> 
            <p>{content.title}</p>
        </div>   
        {/each}
    </div>
</div>





<!-- Diese page.svelte als Willkommenseite definieren, Viel Spaß bei Pingu Run! - ButtonClick und los gehts -->