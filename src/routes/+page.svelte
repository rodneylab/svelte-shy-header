<script>
	import Header from '$lib/components/Header.svelte';
	import '@fontsource/playfair-display/latin.css';
	import '$lib/styles/global.css';
</script>

<Header />
<main class="container" />

<style>
	.container {
		height: 500vh;
		width: var(--max-width-full);

		/* CREDIT: https://www.svgbackgrounds.com/ */
		background-color: #3d315b;
		background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='600' height='100' viewBox='0 0 600 100'%3E%3Cg stroke='%23FFF' stroke-width='0' stroke-miterlimit='10' %3E%3Ccircle fill='%23FB5607' cx='0' cy='0' r='50'/%3E%3Ccircle fill='%23FC7839' cx='100' cy='0' r='50'/%3E%3Ccircle fill='%23F92A82' cx='200' cy='0' r='50'/%3E%3Ccircle fill='%23F9EA92' cx='300' cy='0' r='50'/%3E%3Ccircle fill='%23F4DA52' cx='400' cy='0' r='50'/%3E%3Ccircle fill='%23EFCA08' cx='500' cy='0' r='50'/%3E%3Ccircle fill='%23FB5607' cx='600' cy='0' r='50'/%3E%3Ccircle cx='-50' cy='50' r='50'/%3E%3Ccircle fill='%23fc6824' cx='50' cy='50' r='50'/%3E%3Ccircle fill='%23ff505a' cx='150' cy='50' r='50'/%3E%3Ccircle fill='%233D315B' cx='250' cy='50' r='50'/%3E%3Ccircle fill='%23f6e273' cx='350' cy='50' r='50'/%3E%3Ccircle fill='%23f1d237' cx='450' cy='50' r='50'/%3E%3Ccircle fill='%23fa9500' cx='550' cy='50' r='50'/%3E%3Ccircle cx='650' cy='50' r='50'/%3E%3Ccircle fill='%23FB5607' cx='0' cy='100' r='50'/%3E%3Ccircle fill='%23FC7839' cx='100' cy='100' r='50'/%3E%3Ccircle fill='%23F92A82' cx='200' cy='100' r='50'/%3E%3Ccircle fill='%23F9EA92' cx='300' cy='100' r='50'/%3E%3Ccircle fill='%23F4DA52' cx='400' cy='100' r='50'/%3E%3Ccircle fill='%23EFCA08' cx='500' cy='100' r='50'/%3E%3Ccircle fill='%23FB5607' cx='600' cy='100' r='50'/%3E%3Ccircle cx='50' cy='150' r='50'/%3E%3Ccircle cx='150' cy='150' r='50'/%3E%3Ccircle cx='250' cy='150' r='50'/%3E%3Ccircle cx='350' cy='150' r='50'/%3E%3Ccircle cx='450' cy='150' r='50'/%3E%3Ccircle cx='550' cy='150' r='50'/%3E%3C/g%3E%3C/svg%3E");
	}
</style>
