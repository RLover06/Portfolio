<script lang="ts">
	export let col_1: string = '';
	export let col_2: string = '';
	export let col_3: string = '';
</script>

<li>
	<div class="flex gap-3">
		<p class="font-bold text-indigo-300">{col_1}</p>
		<p class="text-slate-100 italic">{col_2}</p>
		<p>{col_3}</p>
	</div>
</li>
