<script>
	import Note from './Note.svelte';

	export let text = 'Milk';
	export let checked = false;
	export let noteIndex = 0;
	export let totalNotes = 0;
</script>

<Note {noteIndex} {totalNotes}>
	<div class="checkboxContainer">
		<input class="noteCheckbox" type="checkbox" bind:checked />
		<input class="noteText" class:checked disabled={checked} type="text" bind:value={text} />
	</div>
</Note>

<style>
	.checkboxContainer {
		width: 100%;
		height: 100%;
		padding: 0 10px;
		display: grid;
		grid-template-columns: 25px 1fr;
		column-gap: 10px;
		align-items: center;
		justify-items: center;
	}

	.noteCheckbox {
		width: 25px;
		height: 25px;
	}

	.noteText {
		height: 30px;
		width: 100%;
	}

	.checked {
		text-decoration: line-through;
		opacity: 50%;
	}
</style>
