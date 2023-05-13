<script lang="ts">
    
	import AboutMe from "$lib/components/AboutMe.svelte";
	import ProfExp from "$lib/components/ProfExp.svelte";
    import Sidebar from "../lib/components/Sidebar.svelte";
    export let data;
    const{ personalData, aboutMe } = data;
</script>

<div class="flex flex-col sm:flex-row">
    <Sidebar {personalData} />
    <section class="p-8 sm:p-16 w-full sm:basis-2/3 ml-auto">
        <AboutMe data={aboutMe} />
        <ProfExp />
        <div class="flex w-full flex-wrap">

            <h2 class="text-lg font-bold text-center">Con gusto puedo complementar la informacion que consideren pertinenteS</h2>
        </div>

    </section>
</div>
