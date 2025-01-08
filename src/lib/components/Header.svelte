<script lang="ts">
	/* This is code is based on an adaptation by https://twitter.com/jaffathecake of
	https://jsbin.com/mamisar/edit?html,css,js,output By https://twitter.com/flackrw 
	*/
	import { onMount } from 'svelte';

	let header: HTMLDivElement | null = $state(null);
	let headerHeight = $state(165);
	let headerShifterHeight = $state(0);

	function fixHeaderOffset() {
		if (header) {
			header.style.setProperty('--computed-height', `${headerHeight}px`);

			headerShifterHeight =
				Math.min(
					header.offsetTop,
					document.documentElement.scrollHeight - window.innerHeight - headerHeight,
				) - 1;
		}
	}

	onMount(() => {
		if (header) {
			header.style.position = 'sticky';
			header.style.top = 'calc(var(--_computed-height) * -1 - 1px)';
			header.style.bottom = 'calc(100% - var(--_computed-height))';
			fixHeaderOffset();
		}
	});
</script>

<svelte:window on:scroll={fixHeaderOffset} on:resize={fixHeaderOffset} />

<div style:height="{headerShifterHeight}px" class="header-shifter"></div>
<div
	bind:this={header}
	bind:clientHeight={headerHeight}
	style:margin-bottom="-{headerShifterHeight}px"
	class="header"
>
	<header class="wrapper">☺️ Svelte Shy Header 🙈</header>
</div>

<style>
	.header-shifter {
		background-color: var(--colour-dark);
	}
	.header {
		--_computed-height: var(--computed-height, 165px);
		position: relative;
		background: var(--colour-dark);
		color: var(--colour-brand);
		padding: var(--spacing-6);
	}
	.wrapper {
		width: var(--max-width-full);
		margin: var(--spacing-6) auto;
		max-width: var(--max-width-full);
		font-size: var(--font-size-6);
		font-weight: var(--font-weight-bold);
		text-align: center;
	}
</style>
