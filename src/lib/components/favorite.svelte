<script lang="ts">
	export let col_1: string = '';
	export let col_2: string = '';
	export let col_3: string = '';
</script>

<li class="py-2 border-b border-slate-800">
	<div class="grid grid-cols-2 gap-3">
		<p class="font-bold text-indigo-300">
			{col_1}
		</p>
		<p class="hidden md:block text-slate-100 italic">
			{col_2}
		</p>
		{#if col_3}
			<p>
				{col_3}
			</p>
		{/if}
	</div>
</li>
