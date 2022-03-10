<script>
	import NormalizeCSS from '$lib/styles/NormalizeCSS.svelte';
	import GlobalCSS from '$lib/styles/GlobalCSS.svelte';
	import ImportVariablesCSS from '$lib/styles/ImportVariablesCSS.svelte';

	import Header from '$lib/header/Header.svelte';
	import Footer from '$lib/footer/Footer.svelte';
</script>

<svelte:head>
	<script src="https://kit.fontawesome.com/9ab846a867.js" crossorigin="anonymous"></script>
</svelte:head>

<!-- CSS -->
<NormalizeCSS />
<GlobalCSS />
<ImportVariablesCSS />

<!-- Content -->
<Header />
<main>
	<slot />
</main>
<Footer />

<style>
	:global(body) {
		display: grid;
		grid-template-areas: 'header content footer';
	}

	main {
		width: 100vw;
		min-height: calc(100vh - var(--header-height) - var(--footer-height));
		grid-area: content;
		background-color: var(--color-secondary);
	}
</style>
