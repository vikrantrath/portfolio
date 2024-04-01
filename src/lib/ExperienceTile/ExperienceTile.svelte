<script lang="ts">
	import type { Experience } from '$lib/@types/Experience';
	import Skills from '$lib/About/Skills/Skills.svelte';

	export let experience: Experience;
</script>

<a href={experience.link} class="experience-tile p-4" target="_blank">
	<div class="flex gap-x-4 gap-y-4">
		<div class="w-1/3">
			<span class="mx-2 year">{experience.startYear}</span>-<span class="mx-2 year"
				>{experience.endYear}</span
			>
		</div>
		<div class="w-2/3">
			<span class="title">{experience.title}</span>
			<p class="mt-4">{experience.description}</p>
			<Skills skills={experience.skills} />
		</div>
	</div>
</a>

<style lang="scss">
	.experience-tile:hover {
		background: rgba(255, 255, 255, 0.05);
		border-radius: 1rem;
		box-shadow:
			0 4px 8px 0 rgba(0, 0, 0, 0.2),
			0 6px 20px 0 rgba(0, 0, 0, 0.19);

		.title {
			color: rgb(94, 234, 212);
		}
	}

	.year {
		color: rgb(147 162 183);
	}
</style>
