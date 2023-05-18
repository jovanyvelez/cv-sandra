<script>
	import { muestras } from '$lib/datos/info';
</script>

<div class="my-10">
	<h2 class="font-bold">{muestras[0].title}</h2>
    {#each muestras as muestra }
        
	<ul class="ml-5">
        
        <li class="font-bold text text-2xl">{muestra.primera}:</li>
		
        <ul class="ml-5 text-xl mb-5">
            <li>{muestra.estado}</li>
			<li class="ml-2 text-blue">
                <span class="text-black">🕸️ github: </span><a href={muestra.github}>{muestra.github}</a>
			</li>
			<li class="ml-2 text-blue">
                <span class="text-black">🕸️ Web: </span><a href={muestra.web}>{muestra.web}</a>
			</li>
			<li class="text-sm"><span class="font-bold">Nota:</span> {muestra.notas}</li>
		</ul>

	</ul>
    {/each}
</div>
