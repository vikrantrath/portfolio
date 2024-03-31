<script lang="ts">
	import Nested from '$lib/Nested/Nested.svelte';
	let name: string = 'Vikrant';
</script>

<h1>Changing content with {name.toUpperCase()}</h1>
<Nested />

<style lang="scss">
	h1 {
		font-weight: 200;
	}
</style>
