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
			description: `Welcome to our niche tech blog, a passion project built with Angular, TypeScript, & Bootstrap.
			 Dive into exclusive articles tailored to tech enthusiasts like you. 
			 Join us on this journey of discovery as we explore the latest trends and insights in technology together!`,
			link: 'https://fullstackfoodieblog.netlify.app/'
		},
		{
			imageUrl: sheerImg,
			title: 'Sheer Analytics and Insights',
			description: `Freelance project: a user-friendly report-generating website powered by GatsbyJs. 
			Optimized for SEO, it features market research articles available for purchase.
			Elevate your online presence effortlessly!`,
			link: 'https://www.sheeranalyticsandinsights.com/'
		},
		{
			imageUrl: spotify,
			title: 'Spotify Vue',
			description: `Discover our Vue3-based Spotify replica, built from scratch.
			 			Dive deep into Vue3's features with our comprehensive test suite.
			 			 Join us in exploring the world of music streaming development!`,
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
