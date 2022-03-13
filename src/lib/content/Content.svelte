<div>
	<main>
		<slot />
	</main>
</div>

<style>
	div {
		display: flex;
		justify-content: center;
		grid-area: content;
		width: 100vw;
		min-height: calc(100vh - var(--header-height) - var(--footer-height));
		background-color: var(--color-secondary);
	}

	main {
		max-width: 1200px;
		width: 100%;
		height: 100%;
	}
</style>
