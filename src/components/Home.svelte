<script>
    import Video from "./Video.svelte";
    let show = false;

</script>


<p class="text-center mx-auto">hello</p>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>


<button on:click={()=>show = !show}>
    <p class="bg-pink-100">button</p>
</button>

{#if show}
    <Video src="/demo.mp4" muted/>
{/if}