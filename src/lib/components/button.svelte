<script lang="ts">
	export let text: string = '';
	export let href: string = '';
	export let targetBlank: boolean = false;
	export let bgColor: string = '';
	export let bgDepthColor: string = '';
	export let disableLink: boolean = false;
</script>

{#if !disableLink}
	<a {href} target={targetBlank ? '_blank' : ''} class="no-underline">
		<button class="pushable font-bold" style="background: {bgDepthColor}">
			<span class="front" style="background: {bgColor};">{text}</span>
		</button>
	</a>
{:else}
	<button class="pushable font-bold" style="background: {bgDepthColor}; text-decoration: none;">
		<span class="front" style="background: {bgColor};">{text}</span>
	</button>
{/if}

<style>
	.pushable {
		background: hsl(340, 97%, 38%);
		border-radius: 12px;
		border: none;
		padding: 0;
		cursor: pointer;
		outline-offset: 4px;
	}
	.front {
		display: block;
		padding: 4px 12px;
		border-radius: 12px;
		font-size: 1rem;
		background: hsl(349, 98%, 58%);
		color: white;
		transform: translateY(-3px);
	}

	.pushable:active .front {
		transform: translateY(-2px);
	}

	a {
		text-decoration: none;
	}

	button {
		text-decoration: none;
	}

	button:hover {
		text-decoration: none;
	}
</style>
