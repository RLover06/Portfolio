<script lang="ts">
	import Icon from './icon.svelte';

	export let title: string = '';
	export let category: string = '';
	export let description: string = '';
	export let linkURL: string = '';
	export let imgURL: string = '';
	export let icons: any[] = [];
</script>

<article class="flex flex-col items-start justify-between">
	<div class="relative w-full">
		<img src={imgURL} alt="" class="aspect-[16/9] w-full rounded-2xl bg-gray-100 object-cover sm:aspect-[2/1] lg:aspect-[3/2] glow-box" />
		<div class="absolute inset-0 rounded-2xl ring-1 ring-inset ring-gray-900/10" />
	</div>
	<div class="max-w-xl">
		<div class="mt-8 mb-2 flex items-center gap-x-4 text-xs">
			<span class="my-1 text-lg bg-gradient-to-r from-green-600 via-green-400 to-green-400 text-transparent bg-clip-text">{category}</span>
		</div>
		<div class="group relative">
			<h3 class="mt-3 text-2xl font-semibold leading-6 bg-gradient-to-r from-indigo-500 via-sky-200 to-white text-transparent bg-clip-text">
				<a href={linkURL} target="_blank">
					{title}
				</a>
			</h3>
			<p class="mt-5 line-clamp-3 text-sm leading-6 bg-gradient-to-r from-slate-500 via-slate-300 to-white text-transparent bg-clip-text">
				{description}
			</p>
		</div>
		<div class="my-8 grid grid-cols-5 gap-2">
			{#each icons as data}
				<div class="m-2">
					<Icon name={data.name} linkURL={data.linkURL} imgURL={data.imgURL} />
				</div>
			{/each}
		</div>
	</div>
</article>
