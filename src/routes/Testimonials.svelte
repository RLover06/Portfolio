<script>
	import { animate, stagger, inView } from 'motion';
	import { onMount } from 'svelte';
	const testimonials = [
		{
			text: "What really distinguishes Over Regino is his talent for explaining complex concepts in a simple and clear way. He is an excellent presenter who made sure every stakeholder was aligned with the progress and technical aspects. His consistent updates and solution-oriented mindset made the collaboration seamless and highly effective. I strongly recommend Over Regino for any Svelte or React.js project. He is a dependable, skilled professional who consistently delivers outstanding results. I would gladly work with him again!",
			author: 'David Montes',
			company: 'AfterLib',
			image: 'david-montes.jpg',
		},
		{
			text: "Collaborating with Over Regino on the ChatNode web app has been an excellent experience. He is dependable, fast at resolving issues, and consistently contributes thoughtful insights to the project. His communication skills are outstanding as well! Having him on the team has been a real advantage, and his work has been key in delivering many new features to ChatNode.",
        	author: 'Sacha Dumay',
			company: 'Chatnode.ai',
			image: 'sacha.jpg',
		},
		{
			text: 'It was a pleasure collaborating with Over Regino, and we successfully brought the project to completion. He is a highly skilled professional who followed our requirements closely and delivered excellent results.',
          	author: 'Michael Makedonsky',
			company: 'Agatha Global Tech',
			image: '/michael.png',
		},
		{
			text: "Working with Over Regino was a truly fantastic experience. He demonstrates a strong work ethic, is very responsive, and communicates effectively. He achieved excellent results and integrated seamlessly with the team.",
			author: 'Josh Yang',
			company: 'MLytica',
			image: '/josh.jpg',
		},
	];

	onMount(() => {
		inView('#animation-trigger', () => {
			animate('figure', { opacity: 1, y: [25, 0] }, { delay: stagger(0.15) });
		});
	});
</script>

<div class="relative isolate pb-16">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="mx-auto max-w-xl text-center">
			<h2
				id="testimonials-title"
				class="text-3xl font-bold tracking-tight text-center sm:text-4xl bg-gradient-to-r text-indigo-300 glow space-grotesk"
			>
				Testimonials
			</h2>
		</div>
		<div class="relative isolate mx-auto mt-8 grid grid-cols-1 gap-8 sm:grid-cols-2 max-w-6xl">
			<div id="animation-trigger" class="h-1 w-full absolute top-[30rem]" />
			{#each testimonials as { text, author, company, image }, i}
				<figure
					class="group rounded-2xl bg-gradient-to-tl from-slate-800 to-slate-600 p-6 shadow-lg ring-1 ring-gray-900/5 flex flex-col h-full flex-grow hover:outline-dotted hover:outline-4 outline-indigo-400 outline-offset-4"
				>
					<blockquote class="text-gray-400 font-semibold text-base flex-grow">
						<p>"{text}"</p>
					</blockquote>
					<figcaption class="mt-6 flex items-center gap-x-4">
						<img class="h-10 w-10 rounded-full bg-gray-50 group-hover:motion-preset-shake" src={image} alt="" />
						<div>
							<div class="font-semibold text-gray-300">{author}</div>
							<div class="text-gray-300">{company}</div>
						</div>
					</figcaption>
				</figure>
			{/each}
		</div>
	</div>
</div>
