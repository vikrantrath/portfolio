<script lang="ts">
	import Navbar from '$lib/Navbar/Navbar.svelte';
	import { onMount } from 'svelte';
	import '../app.css';

	onMount(() => {
		window.addEventListener('mousemove', handleGradient);

		return () => {
			window.addEventListener('mousemove', handleGradient);
		};
	});

	function handleGradient(this: Window, ev: MouseEvent) {
		this.document
			.getElementById('main')
			?.setAttribute(
				'style',
				`background:radial-gradient(600px at ${ev.clientX}px ${ev.clientY}px, rgba(29, 78, 216, 0.15), transparent 80%);`
			);
	}
</script>

<div id="main">
	<Navbar />
	<div
		class="mx-auto min-h-screen max-w-screen-xl px-6 py-12 font-sans md:px-12 md:py-20 lg:px-24 lg:py-0"
	>
		<slot />
	</div>
</div>

<style lang="postcss">
	:global(html),
	:global(body),
	:global(#main) {
		background-color: rgb(15, 23, 42);
		margin: 0;
		/* height: 100%; */
		width: 100%;
		color: rgb(226, 232, 240);
	}	
</style>
