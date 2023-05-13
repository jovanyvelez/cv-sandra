<script>
	import Skills from "$lib/components/Skills.svelte";

    export let data;
    const {title, body} = data;
</script>

<div>
    <h2 class="mb-8 font-bold">{title}</h2>
    {#each body as e (e.id)}
        <p class="mb-6">{e.paragraph}</p>
    {/each}
    <Skills />
</div>