<script>
	import Button from '$lib/shared/Button.svelte';
	import Icon from '$lib/shared/Icon.svelte';
</script>

<div class="container">
	<Button link round width="50px" height="50px">
		<Icon icon="fa-solid fa-plus" size="32px" />
	</Button>
</div>

<style>
	.container {
		grid-area: buttons;
		padding: 15px;
		display: grid;
		color: var(--color-primary);
	}
</style>
