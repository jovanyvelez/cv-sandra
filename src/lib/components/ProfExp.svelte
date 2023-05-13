<script lang="ts">
    import { professionalData } from '$lib/datos/info'
    const {title, experiences} = professionalData;
</script>

<section>
    <h2 class="my-6 font-bold">{title}</h2>
    <div class="flex flex-col gap-6">
        {#each experiences as experience (experience.id) }
            <div class="flex flex-col rounded-lg">
                <span class={`h-2 ${experience.current? 'bg-green':'bg-grey'}   `}/>
                <div class="bg-grey-light p-6 drop-shadow-md">
                    <h3 class="font-bold">{experience.role}</h3>
                    <p class="mt-2">{experience.description}</p>
                </div>
            </div>
        {/each}
    </div>
</section>
