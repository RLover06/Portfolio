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
	<div bind:this={tooltip} class="fixed py-2 text-indigo-200 text-lg italic" style="display: none;">{name}</div>
	<a bind:this={referenceElement} href={linkURL} target="_blank">
		<img class="h-12 col-span-1 mx-auto flex justify-center shake-on-hover" src={imgURL} alt="" />
	</a>
</div>
