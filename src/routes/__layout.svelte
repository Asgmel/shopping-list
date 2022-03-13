<script>
	import NormalizeCSS from '$lib/styles/NormalizeCSS.svelte';
	import GlobalCSS from '$lib/styles/GlobalCSS.svelte';
	import ImportVariablesCSS from '$lib/styles/ImportVariablesCSS.svelte';

	import Header from '$lib/header/Header.svelte';
	import Footer from '$lib/footer/Footer.svelte';
	import Container from '$lib/content/Content.svelte';
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
<Container>
	<slot />
</Container>
<Footer />

<style>
	:global(body) {
		display: grid;
		grid-template-areas: 'header' 'content' 'footer';
	}
</style>
