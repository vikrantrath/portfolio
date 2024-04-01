<script lang="ts">
	export let skills: string[];
</script>

<div class="mt-4 max-w-xs leading-normal">
	<div class="skill-box p-4 mt-4 flex flex-wrap gap-4">
		{#each skills as skill}
			<span class="p-2 skill">{skill}</span>
		{/each}
	</div>
</div>

<style lang="scss">
	.skill-box {
		border: solid 0.1rem rgb(94, 234, 212);
		border-radius: 1.5rem;
	}

	.skill {
		background: rgba(94, 234, 212, 0.1);
		border-radius: 1rem;
		color: rgb(94, 234, 212);
	}
</style>
