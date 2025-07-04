<script lang="ts">
	import { onMount, onDestroy } from 'svelte';
	import { createPopper } from '@popperjs/core';

	export let name: string = '';
	export let linkURL: string = '';
	export let imgURL: string = '';

	let tooltip: HTMLElement;
	let referenceElement: HTMLElement;
	let popperInstance: any = null;
	let tooltipTimeout: ReturnType<typeof setTimeout>;

	function showTooltip() {
		tooltipTimeout = setTimeout(() => {
			tooltip.style.display = 'block';
			popperInstance.update();
		}, 100);
	}

	function hideTooltip() {
		clearTimeout(tooltipTimeout);
		tooltip.style.display = 'none';
	}

	function initializePopper() {
		try {
			popperInstance = createPopper(referenceElement, tooltip, {
				placement: 'top',
			});
			tooltip.style.display = 'none';
		} catch (error) {
			console.error('Popper initialization error:', error);
		}
	}

	function addEventListeners() {
		referenceElement.addEventListener('mouseover', showTooltip);
		referenceElement.addEventListener('mouseout', hideTooltip);
	}

	function removeEventListeners() {
		referenceElement.removeEventListener('mouseover', showTooltip);
		referenceElement.removeEventListener('mouseout', hideTooltip);
	}

	onMount(() => {
		initializePopper();
		addEventListeners();
	});

	onDestroy(() => {
		removeEventListeners();
	});
</script>

<div class="my-2">
	<div
		bind:this={tooltip}
		class="fixed py- text-indigo-300 text-lg font-semibold glow space-grotesk"
		style="display: none;"
	>
		{name}
	</div>
	<a bind:this={referenceElement} href={linkURL} target="_blank">
		<img
			class="h-14 p-2 col-span-1 mx-auto flex justify-center object-cover bg-gradient-to-b from-slate-500 to bg-slate-700 rounded-lg hover:motion-preset-shake border border-1 border-slate-500 shadow-md shadow-neutral-700
			{name === 'Docker' ? 'p-0' : 'p-2'}"
			src={imgURL}
			alt=""
		/>
	</a>
</div>
