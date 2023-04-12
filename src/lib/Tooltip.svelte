<script>
	import { onMount } from 'svelte';

	export let tip = '';
	export let active = false;

	let loaded = false;
	onMount(() => (loaded = true));
</script>

<!-- preventing layout shifts by checking if page is fully loaded. if not, return original slot -->
{#if loaded && tip}
	<div class="tooltip-wrapper">
		<span class="tooltip" class:active>
			{tip}
		</span>
		<span class="tooltip-slot">
			<slot />
		</span>
	</div>
{:else}
	<slot />
{/if}

<style lang="scss">
	.tooltip-wrapper {
		position: relative;
		display: inline-block;
		
		&:hover .tooltip {
			opacity: 1;
			visibility: initial;
			margin-top: -.3rem;
		}
	}

	.tooltip {
		position: absolute;
		display: inline-block;
		white-space: nowrap;
		opacity: 0;
		visibility: hidden;
		transition: opacity 0.2s ease-in-out, visibility 0.2s ease-in-out, margin-top 0.2s ease-in-out;
		left: 50%;
		top: 0%;
		line-height: normal;
		transform: translate(-50%, -120%);
		padding: 0.18rem 0.5rem;
		border-radius: 4px;
		border: 2px solid rgb(33, 33, 37);
		background: rgb(39, 39, 42);
		color: rgb(255, 255, 255);
		font-size: 0.94rem;
		font-weight: 500;

		// the little triangle below the tooltip v
		&::after {
			border-left: solid transparent 10px;
			border-right: solid transparent 10px;
			border-top: solid rgb(39, 39, 42) 10px;
			bottom: -8px;
			content: ' ';
			height: 0;
			width: 0;
			left: 50%;
			margin-left: -10px;
			position: absolute;
		}

		&.active {
			opacity: 1;
			visibility: initial;
			margin-top: -8px;
		}
	}
</style>
