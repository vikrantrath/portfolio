<script lang="ts">
	import type { Experience } from '$lib/@types/Experience';
	import ExperienceTile from '$lib/ExperienceTile/ExperienceTile.svelte';

	const experiences: Experience[] = [
		{
			startYear: '2021',
			endYear: 'Present',
			title: 'Senior Full Stack Engineer, Morgan Stanley',
			description: `Build and maintain critical components for Morgan Stanley, across multiple products.
                 Work with industry professionals to implement best practices and scalable solutions. 
                 Knowledge share bleeding edge technological advancements,
                mentor interns and junior developers to help upskill professionals at grass root level.`,
			skills: ['JavaScript', 'Java', 'SpringBoot', 'ReactJS', 'Python', 'GIT', 'VueJS', 'Figma'],
			link: 'https://www.morganstanley.com'
		},
		{
			startYear: '2018',
			endYear: '2021',
			title: 'Full Stack Engineer, Allstate',
			description: `Learn and eventually create industry standard solutions for Allstate, across multiple insurance products.
                 Work with industry professionals to implement best practices and scalable solutions. 
                Help train engineers in different domains to be Full-Stack Developers.`,
			skills: ['JavaScript', 'Java', 'SpringBoot', 'ReactJS', 'NodeJS', 'GIT', 'Figma'],
			link: 'https://www.allstate.com'
		}
	];
</script>

<div class="about lg:flex lg:gap-4 justify-center items-center flex-col mt-12">
	<div class="flex flex-col gap-12 lg:w-1/2">
		{#each experiences as experience}
			<ExperienceTile {experience} />
		{/each}
	</div>
</div>
