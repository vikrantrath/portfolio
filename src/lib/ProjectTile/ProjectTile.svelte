<script lang="ts">
	import type { Tile } from '$lib/@types/Tile';
	import openLogo from '$lib/assets/open.svg';
	export let tile: Tile;
</script>

<div class="container flex gap-8">
	<img class="w-1/2  max-h-40" src={tile.imageUrl} alt={`project-${tile.title}`} />
	<div class="flex flex-col w-1/2">
		<span class="text-lg font-medium tracking-tight text-slate-200 sm:text-xl flex items-center gap-4"
			>{tile.title}<a class="h-6" href={tile.link} target="_blank"><img src={openLogo} alt="open" /></a></span
		>
		<p>{tile.description}</p>
	</div>
</div>
