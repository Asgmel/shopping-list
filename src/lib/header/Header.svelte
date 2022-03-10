<script>
	import Logo from './Logo.svelte';
	import Profile from './Profile.svelte';
	import Buttons from './Buttons.svelte';
</script>

<header>
	<Logo />
	<Buttons />
	<Profile />
</header>

<style>
	header {
		width: 100vw;
		height: var(--header-height);
		background-color: var(--color-secondary);
		grid-area: header;
		display: grid;
		grid-template-columns: min-content 1fr min-content min-content;
		grid-template-areas: 'logo . buttons profile';
	}
</style>
