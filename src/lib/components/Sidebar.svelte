<script lang="ts">
	import Envelope from "$lib/components/icons/Envelope.svelte";
    import type {DatosPersonales} from '$lib/types/DatosPersonales';
	import Phone from "./icons/Phone.svelte";
    export let personalData:DatosPersonales;
    const {name, role, education, contactLinks} = personalData;
</script>

<div class="bg-black flex flex-col content-between w-full h-auto sm:h-screen sm:justify-evenly sm:w-1/3 sm:fixed sm:mx-2" >
    <div class="text-white flex flex-col p-10 items-center">
        <input type="image" src = {'/images/jovany.jpg'} alt="foto jovany" width="200" height="200" class="rounded-full h-full mb-6"/>
        <h1 class="mb-2 sm:text-2xl text-center">{name}</h1>
        <h2 class="mb-8">{role}</h2>
        <p class="mb-2">{education[0]}</p>
        <div class="text-white text-center mb-4 mt-4 sm:mt-8">
            <h3>CONTACTAME</h3>
            <div class="flex justify-center gap-3">
                <h3 class="text-3xl" > <Envelope/>  </h3>
                <h3>{contactLinks?.[0]}</h3>
            </div>
            <div class="flex justify-center gap-3">
                <h3 class="text-3xl" > <Phone/>  </h3>
                <h3>{contactLinks?.[1]}</h3>
            </div>

        </div>
    </div>

</div>