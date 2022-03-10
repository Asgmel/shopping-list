<script>
	import theme from '$lib/styles/defaultTheme';

	export let link = false;
	export let href = '/';
	export let round = false;
	export let width = 'auto';
	export let height = 'auto';
	export let backgroundColor = theme['--color-secondary'];
	export let color = theme['--color-primary'];
	export let hoverBackground = theme['--color-tertiary'];
</script>

{#if link}
	<a {href}>
		<div
			class="button"
			class:round
			style="--button-width: {width}; 
                    --button-height: {height};
                    --button-color: {color};
                    --button-background-color: {backgroundColor};
                    --button-hover-background: {hoverBackground};"
		>
			<slot />
		</div>
	</a>
{:else}
	<button
		class:round
		class="button"
		style="--button-width: {width};
                --button-height: {height};
                --button-color: {color};
                --button-background-color: {backgroundColor};
                --button-hover-background: {hoverBackground};"
	>
		<slot />
	</button>
{/if}

<style>
	a {
		text-decoration: none;
		color: inherit;
	}

	.button {
		display: flex;
		align-items: center;
		justify-content: center;
		background-color: var(--button-background-color);
		color: var(--button-color);
		height: var(--button-height);
		width: var(--button-width);
	}

	.button:hover {
		background-color: var(--button-hover-background);
	}

	.round {
		border-radius: 100%;
	}
</style>
