<script lang="ts">
	import type { Tile } from '$lib/@types/Tile';
	import ProjectTile from '$lib/ProjectTile/ProjectTile.svelte';
	import blogImg from '$lib/assets/blog.png';
	import sheerImg from '$lib/assets/sheer.png';
	import spotify from '$lib/assets/spotify.png';
	import arrowLeftIcon from '$lib/assets/arrow-left.svg';

	const tiles: Tile[] = [
		{
			imageUrl: blogImg,
			title: 'Full Stack Foodie Blog',
			description: 'A blog with technology articles built with Angular',
			link: 'https://fullstackfoodieblog.netlify.app/'
		},
		{
			imageUrl: sheerImg,
			title: 'Sheer Analytics and Insights',
			description: 'A report generating website built for users using GatsbyJs',
			link: 'https://www.sheeranalyticsandinsights.com/'
		},
		{
			imageUrl: spotify,
			title: 'Spotify Vue',
			description: 'A replica of spotify built on Vue3 from scratch',
			link: 'https://github.com/vikrantrath/spotify-vue'
		}
	];
</script>

<div class="about lg:flex lg:gap-4 justify-center items-center flex-col mt-12">
	<div class="flex justify-center items-center flex-col gap-8">
		{#each tiles as tile (tile.title)}
			<ProjectTile {tile} />
		{/each}
	</div>

	<a class="mt-4 flex gap-1" href="https://github.com/vikrantrath" target="_blank"
		>View All Projects <img class="w-5 pt-1" src={arrowLeftIcon} alt="arrow-left" /></a
	>
</div>
