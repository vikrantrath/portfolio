<script lang="ts">
	export let tooltipText: string;
</script>

<div class="tooltip">
	<slot />
	<span class="tooltiptext">{tooltipText}</span>
</div>

<style>
	/* Tooltip container */
	.tooltip {
		position: relative;
		display: inline-block;
	}

	/* Tooltip text */
	.tooltip .tooltiptext {
		visibility: hidden;
		background-color: rgb(226, 232, 240);
		color: rgb(15, 23, 42);
		text-align: center;
		padding: 0.2rem 1rem;
		border-radius: 6px;
        max-width: 20rem;
        max-height: 3rem;
        display: flex;

		/* Position the tooltip text - see examples below! */
		position: absolute;
		z-index: 1;
	}

	/* Show the tooltip text when you mouse over the tooltip container */
	.tooltip:hover .tooltiptext {
		visibility: visible;
	}
</style>
