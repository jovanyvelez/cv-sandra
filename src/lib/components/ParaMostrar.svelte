<script>
	import { muestras } from '$lib/datos/info';
	const { title, primera, estado, github, web, notas } = muestras;
</script>

<div class="my-10">
	<h2 class="font-bold">{title}</h2>
	<ul class="ml-5">
		<li class="font-bold text text-2xl">{primera}:</li>
		<ul class="ml-5 text-xl">
			<li>{estado}</li>
			<li class="ml-2 text-blue">
				<span class="text-black">🕸️ github: </span><a href={github}>{github}</a>
			</li>
			<li class="ml-2 text-blue">
				<span class="text-black">🕸️ Web</span><a href={web}>{web}</a>
			</li>
			<li class="text-sm"><span class="font-bold">Nota:</span> {notas}</li>
		</ul>
	</ul>
</div>
