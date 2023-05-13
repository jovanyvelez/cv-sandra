<script>
	import { activeTab } from '$lib/store';
	import { skills } from '$lib/datos/info';
	const { soft, hard } = skills;
</script>

<div class="flex">
	<button
		type="button"
		on:click={() => {
			$activeTab = 'soft';
		}}
		class={`btn ${$activeTab !== 'soft' ? 'bg-grey' : 'bg-yellow'}`}>Habilidades Sociales</button
	>
	<button
		type="button"
		on:click={() => {
			$activeTab = 'hard';
		}}
		class={`btn ${$activeTab === 'soft' ? 'bg-grey' : 'bg-yellow'}`}>Habilidades Tecnicas</button
	>
</div>

<ul class="flex flex-row flex-wrap content-start list-none py-4 gap-2">
	{#if $activeTab === 'soft'}
		{#each soft as skill (skill.text)}
			<li class="skills"><span>{skill.icon}</span>{skill.text}</li>
		{/each}
	{:else}
		{#each hard as skill (skill.text)}
			<li class="skills"><span>{skill.icon}</span>{skill.text}</li>
		{/each}
	{/if}
</ul>
