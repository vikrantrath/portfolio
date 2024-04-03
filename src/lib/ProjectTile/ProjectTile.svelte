<script lang="ts">
	import type { Tile } from '$lib/@types/Tile';
	export let tile: Tile;
</script>

<a class="container flex gap-8 project-tile p-4 lg:w-3/4" href={tile.link} target="_blank">
	<img class="w-1/2 max-h-40" src={tile.imageUrl} alt={`project-${tile.title}`} />
	<div class="flex flex-col w-1/2">
		<span
			class="text-lg font-medium tracking-tight text-slate-200 sm:text-xl flex items-center gap-4 title"
			>{tile.title}</span
		>
		<p>{tile.description}</p>
	</div>
</a>

<style lang="scss">
	.project-tile:hover {
		background: rgba(255, 255, 255, 0.05);
		border-radius: 1rem;
		box-shadow:
			0 4px 8px 0 rgba(0, 0, 0, 0.2),
			0 6px 20px 0 rgba(0, 0, 0, 0.19);

		.title {
			color: rgb(94, 234, 212);
		}
	}
</style>
