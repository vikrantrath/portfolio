<script lang="ts">
	let count = 0;
	const increment = () => {
		count += 1;
	};
</script>

<h1 class="child">Child</h1>
<button on:click={increment}>{count}</button>

<style>
	@import './nested.scss';
</style>
