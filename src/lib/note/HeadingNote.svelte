<script>
	import Note from './Note.svelte';

	export let text = '';
	export let noteIndex = 0;
	export let totalNotes = 0;
</script>

<Note {noteIndex} {totalNotes}>
	<div class="headingContainer">
		<input type="text" bind:value={text} />
	</div>
</Note>

<style>
	.headingContainer {
		width: 100%;
		height: 100%;
	}

	input {
		font-size: 20px;
		font-weight: 500;
		margin: 10px 0 10px 12px;
	}
</style>
