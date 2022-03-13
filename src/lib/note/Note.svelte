<script>
	import Icon from '$lib/shared/Icon.svelte';
	export let noteIndex = 0;
	export let totalNotes = 0;
</script>

<div
	class="container"
	class:lastContainer={noteIndex == totalNotes - 1}
	class:firstContainer={noteIndex == 0}
>
	<slot />
	<div class="noteControls">
		<div class="noteMove noteControlButton">
			<Icon icon="fa-solid fa-bars" size="30px" />
		</div>
		<div class="noteDelete noteControlButton">
			<Icon icon="fa-solid fa-xmark" size="30px" />
		</div>
	</div>
</div>

<style>
	.container {
		display: grid;
		grid-template-columns: 1fr 90px;
		column-gap: 10px;
		align-items: center;
		justify-items: center;
		padding: 10px;
	}

	.container:hover {
		border-top: 1px solid rgba(0, 0, 0, 0.2);
		border-bottom: 1px solid rgba(0, 0, 0, 0.2);
		margin: -1px 0;
	}

	.lastContainer {
		border-bottom: none !important;
		margin-bottom: 0 !important;
	}

	.firstContainer {
		border-top: none !important;
		margin-top: 0 !important;
	}

	.container:hover > .noteControls {
		display: grid;
	}

	.noteControls {
		display: grid;
		grid-template-columns: 1fr 1fr;
		align-items: center;
		justify-items: center;
		column-gap: 10px;
		width: 100%;
		height: 100%;
		color: var(--color-error);
	}

	.noteControlButton {
		height: 40px;
		width: 40px;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.noteMove {
		height: 40px;
		width: 40px;
		color: var(--color-primary);
	}

	.noteDelete {
		height: 40px;
		width: 40px;
	}
</style>
