<script lang="ts">
	import Skills from './Skills/Skills.svelte';
	import SocialLinks from './SocialLinks/SocialLinks.svelte';
	import arrowLeftIcon from '$lib/assets/arrow-left.svg';
	import downloadIcon from '$lib/assets/download-icon.svg';

	import './about.scss';
</script>

<div class="about lg:flex lg:justify-between lg:gap-4">
	<div class="lg:sticky lg:top-0 lg:flex lg:max-h-screen lg:w-1/2 lg:flex-col lg:py-24 content-end">
		<h1 class="text-4xl font-bold">Vikrant Rath</h1>
		<h2 class=" mt-3 text-lg font-medium tracking-tight text-slate-200 sm:text-xl">
			Senior Full Stack Engineer
		</h2>
		<p class="mt-4 max-w-xs leading-normal">
			I build fluid, dynamic, and scalable applications with seamless user experiences across the
			frontend and backend.
		</p>
		<SocialLinks />
		<Skills />
		<a class="mt-4 flex gap-1" href="/projects"
			>View My Projects <img class="w-5 pt-1" src={arrowLeftIcon} alt="arrow-left" /></a
		>
	</div>
	<div class="pt-24 lg:w-1/2 lg:py-24">
		<p class="brief">
			As a seasoned <strong>Full-Stack</strong> developer with a proven track record of delivering
			exceptional software solutions, I bring a wealth of expertise in <strong>Java</strong> and
			<strong>JavaScript</strong>
			to the table. With almost <strong>6 years</strong> of hands-on experience in both
			<strong>Front-End</strong>
			and
			<strong>Back-End</strong> development, I possess a deep understanding of modern web technologies
			and frameworks.
		</p>
		<p class="brief">
			My passion for crafting elegant, efficient code is matched only by my commitment to creating
			seamless user experiences that drive engagement and satisfaction. Whether I'm architecting
			scalable backend systems or fine-tuning responsive frontend interfaces, I approach each
			project with a meticulous attention to detail and a relentless pursuit of excellence.
		</p>
		<p class="brief">
			Throughout my career, I have successfully led cross-functional teams, mentored junior
			developers, and collaborated closely with stakeholders to deliver high-impact solutions on
			time and within budget. My ability to adapt to evolving technologies and industry trends,
			combined with my strong problem-solving skills, has enabled me to consistently exceed
			expectations and drive business success.
		</p>
		<p class="brief">
			In addition to my technical prowess, I am known for my strong communication skills,
			collaborative approach, and passion for continuous learning. I thrive in fast-paced,
			collaborative environments where creativity and innovation is encouraged.
		</p>
		<div class="flex flex-col mt-4 gap-4">
			<a class="mt-4 flex gap-1" href="/projects"
				>Resume<img class="w-5" src={downloadIcon} alt="arrow-left" /></a
			>
			<span>Professional Experience</span>
		</div>
	</div>
</div>
