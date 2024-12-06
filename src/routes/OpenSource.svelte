<script>
	import Icon from '$lib/components/Icon.svelte';
	import { onMount } from 'svelte';
	import { animate, stagger, inView } from 'motion';

	const contributions = [
		{
			name: 'Supabase',
			linkURL: 'https://supabase.com/',
			imgURL: 'supabase.png'
		},
		{
			name: 'XYFlow',
			linkURL: 'https://xyflow.com/',
			imgURL: 'xy-flow.png'
		}
	];

	onMount(() => {
		inView('#open-source-end', () => {
			setTimeout(() => {
				animate('#open-source-item', { opacity: 1, y: [25, 0] }, { delay: stagger(0.2) });
			}, 500);
		});
	});
</script>

<div class="pt-4 pb-1 my-24" id="open-source">
	<div class="text-center">
		<h2
			id="open-source-title"
			class="text-3xl font-bold tracking-tight text-center sm:text-4xl bg-gradient-to-r text-indigo-300 glow space-grotesk"
		>
			Open Source Contributions
		</h2>
		<p class="mt-2 text-lg leading-8 text-gray-400">I'm always happy to contribute where I can!</p>
			<div class="mx-auto max-w-7xl py-12 px-4 sm:px-6 lg:px-8">
				<ul class="flex gap-4 justify-center">
					{#each contributions as contribution}
						<li id="open-source-item">
							<Icon
								name={contribution.name}
							linkURL={contribution.linkURL}
								imgURL={contribution.imgURL}
							/>
						</li>
					{/each}
				</ul>
				<div id="open-source-end"></div>
		</div>
	</div>
</div>
