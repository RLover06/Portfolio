<script lang="ts">
	import { onMount, onDestroy } from 'svelte';
	import { createPopper } from '@popperjs/core';

	export let name: string = '';
	export let linkURL: string = '';
	export let imgURL: string = '';

	let tooltip: HTMLElement;
	let referenceElement: HTMLElement;
	let popperInstance: any = null;

	function showTooltip() {
		tooltip.style.display = 'block';
		popperInstance.update();
	}

	function hideTooltip() {
		tooltip.style.display = 'none';
	}

	onMount(() => {
		try {
			popperInstance = createPopper(referenceElement, tooltip, {
				placement: 'top'
			});
			tooltip.style.display = 'none';

			referenceElement.addEventListener('mouseover', showTooltip);
			referenceElement.addEventListener('mouseout', hideTooltip);
		} catch (error) {
			console.error('Popper initialization error:', error);
		}
	});

	onDestroy(() => {
		referenceElement.removeEventListener('mouseover', showTooltip);
		referenceElement.removeEventListener('mouseout', hideTooltip);
	});
</script>

<div class="my-2">
	<div bind:this={tooltip} class="fixed py- text-indigo-300 text-lg font-semibold glow space-grotesk" style="display: none;">{name}</div>
	<a bind:this={referenceElement} href={linkURL} target="_blank">
		<img
			class="h-14 p-2 col-span-1 mx-auto flex justify-center /bg-neutral-600 bg-gradient-to-b from-slate-500 to bg-slate-700 rounded-lg shake-on-hover border border-1 border-slate-500 shadow-md shadow-neutral-700"
			src={imgURL}
			alt=""
		/>
	</a>
</div>
