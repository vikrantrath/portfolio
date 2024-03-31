<script lang="ts">
	import Navbar from '$lib/Navbar/Navbar.svelte';
	import { onMount } from 'svelte';
	import './styles.scss';

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
				`background:radial-gradient(200px at ${ev.clientX}px ${ev.clientY}px, rgba(29, 78, 216, 0.15), transparent 80%);`
			);
	}
</script>

<div id="main">
	<Navbar />
	<slot />
</div>
