<script>
	import CheckboxNote from './CheckboxNote.svelte';
	import HeadingNote from './HeadingNote.svelte';

	const notes = [
		{
			type: 'heading',
			text: 'Birthday Cake',
			checked: false
		},
		{
			type: 'note',
			text: 'Egg',
			checked: false
		},
		{
			type: 'note',
			text: 'Milk',
			checked: false
		},
		{
			type: 'note',
			text: 'Flour',
			checked: false
		},
		{
			type: 'note',
			text: 'Sugar',
			checked: false
		}
	];
</script>

<div class="noteContainer">
	{#each notes as note, i}
		{#if note.type == 'heading'}
			<HeadingNote text={note.text} noteIndex={i} totalNotes={notes.length} />
		{:else}
			<CheckboxNote text={note.text} noteIndex={i} totalNotes={notes.length} />
		{/if}
	{/each}
</div>

<style>
	.noteContainer {
		margin: 20px 0;
		border: 1px solid rgba(0, 0, 0, 0.2);
		border-radius: 0.2rem;
	}
</style>
