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
		</ul>

	</ul>
    {/each}
</div>
