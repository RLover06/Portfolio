<script lang="ts">
	export let text: string = '';
	export let href: string = '';
	export let bgColor: string = '';
	export let bgDepthColor: string = '';
</script>

<a {href} target="_blank">
	<button class="pushable" style="background: {bgDepthColor}"> <span class="front" style="background: {bgColor};">{text}</span></button>
</a>

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
		padding: 12px 42px;
		border-radius: 12px;
		font-size: 1.25rem;
		background: hsl(349, 98%, 58%);
		color: white;
		transform: translateY(-6px);
	}

	.pushable:active .front {
		transform: translateY(-2px);
	}
</style>
