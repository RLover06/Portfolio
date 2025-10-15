<script lang="ts">
	import {
		Accordion,
		AccordionContent,
		AccordionItem,
		AccordionTrigger,
	} from '$lib/components/ui/accordion';
	import Button from '$lib/components/Button.svelte';

	let isHovered: boolean = false;

	const goals = [
		{ icon: '✅', text: "Pirates of the Caribbean: The Curse of the Black Pearl (2003)" },
        { icon: '✅', text: "Pirates of the Caribbean: Dead Man's Chest (2006)" },
        { icon: '✅', text: "Pirates of the Caribbean: At World's End (2007)" },
        { icon: '✅', text: 'Pirates of the Caribbean: On Stranger Tides (2011)' },
        { icon: '🔲', text: "Pirates of the Caribbean: Salazar's Revenge (2017)" },
        ];
</script>

<div
	role="main"
	on:mouseover={() => (isHovered = true)}
	on:mouseout={() => (isHovered = false)}
	on:focus={() => (isHovered = true)}
	on:blur={() => (isHovered = false)}
	class="glow-box mx-2 my-16 rounded-md bg-gradient-to-b from-neutral-100 to-neutral-300 object-cover p-6 py-32 text-left outline-offset-4 outline-indigo-400 hover:outline-dotted hover:outline-4 lg:px-8"
>
	<div class="mx-auto max-w-3xl text-base leading-7 text-gray-700">
		<p class="text-base font-semibold leading-7 text-indigo-600">Bio</p>
		<h1 class="space-grotesk mt-2 text-3xl font-bold tracking-tight text-gray-700 sm:text-4xl">
			Hey there! <span class:wave={isHovered}>👋</span>
		</h1>
		<p class="mt-6 text-xl font-semibold leading-8">
			I am Over Regino, from Monteria, Cordoba - Colombia. As a software developer, 
			I enjoy creating applications of various types in collaboration with people from different
			 parts of the world. 👨🏻‍💻 🌍
		</p>
		<div class="mt-10 max-w-2xl text-lg font-medium">
			<div>
				<p>
    I’m a big admirer of <span class="text-lg font-bold text-black">TypeScript. </span>
    The tools it provides are excellent, but what truly makes it shine is how it helps me
    write code with greater care and intention.

    <br /><br />

    When it comes to frameworks, <span class="text-lg font-bold text-black">🥇 Svelte</span>
    is always my top pick. The developer experience is outstanding, making it a pleasure to use.
    I’m also greatly inspired by
    <span class="italic">Rich Harris</span>
    and all his efforts to advance the framework. For that reason, I built a SvelteKit starter
    template named
    <a class="font-bold" href="https://github.com/RLover06/Portfolio">
        Sveltetastic<span class="font-medium">.</span>
    </a>
    <br /><br />
</p>
<p>
    In second place, I would highlight <span class="text-lg font-bold text-black">🥈 React/Next.js</span>.
    Its vast community and ecosystem are aspects I deeply appreciate.
</p>
<br />

I first came across <span class="text-lg font-bold text-black">Tailwind CSS</span> back in 2019,
and since then it has been my go-to choice. More recently, I’ve been working with
<span class="text-lg font-bold text-black">Shadcn UI</span>, a component library built on Tailwind,
and it has quickly become one of my favorites.


				<div class="flex justify-start">
					<Accordion type="single" collapsible>
						<AccordionItem value="goals" class="border-none">
							<AccordionTrigger class="w-fit  [&>svg]:hidden ">
								<Button
									text={'More'}
									disableLink={true}
									bgColor={'hsl(227, 66%, 55%)'}
									bgDepthColor={'hsl(227, 66%, 25%)'}
								/>
							</AccordionTrigger>
							<AccordionContent
								class="mt-2 rounded-md border-[3px] border-dashed border-indigo-400 p-4"
							>
							<p class="my-4 text-lg font-medium text-black">
                        Even though TypeScript remains my preferred language, lately I’ve been exploring Go.
                       <br /><br />
                       During my free time, I’m usually either developing a project or watching content
                       related to software development. Below are some of my favorite channels:
                          </p>

								<ul class="text-lg font-medium">
									<li>🔵 HunterScript</li>
									<li>🔵 Theo Browne</li>
									<li>🔵 SuperSimpleDev</li>
									<li>🔵 MoureDev by Brais Moure</li>
									<li>🔵 Rich Harris (interviews)</li>
									<li>🔵 Many more...</li>
								</ul>
							</AccordionContent>
						</AccordionItem>
					</Accordion>
				</div>
				<hr class="my-8 border-t-2 border-slate-300" />

				<ul class="mt-8 max-w-2xl space-y-2 text-gray-600">
					<h2 class="space-grotesk mx-auto my-8 text-2xl font-bold tracking-tight text-gray-900">
						The <span class="underline decoration-indigo-600 decoration-wavy underline-offset-8"
						>ideal</span> 
						day looks like...
					</h2>
					<li class="flex gap-x-3">
						<svg
							class="mt-1 h-5 w-5 flex-none text-indigo-600"
							viewBox="0 0 20 20"
							fill="currentColor"
							aria-hidden="true"
						>
							<path
								fill-rule="evenodd"
								d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
								clip-rule="evenodd"
							/>
						</svg>
						<span
							><strong class="font-semibold text-gray-900">Programming.</strong> Building
							applications gives me energy. <span class="text-xl">⚡️</span></span
						>
					</li>
					<li class="flex gap-x-3">
						<svg
							class="mt-1 h-5 w-5 flex-none text-indigo-600"
							viewBox="0 0 20 20"
							fill="currentColor"
							aria-hidden="true"
						>
							<path
								fill-rule="evenodd"
								d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
								clip-rule="evenodd"
							/>
						</svg>
						<span
						><strong class="font-semibold text-gray-900">Reading in English.</strong> An excellent approach to
						 broaden comprehension. <span class="text-xl">📈</span></span	
						>
					</li>
					<li class="flex gap-x-3">
						<svg
							class="mt-1 h-5 w-5 flex-none text-indigo-600"
							viewBox="0 0 20 20"
							fill="currentColor"
							aria-hidden="true"
						>
							<path
								fill-rule="evenodd"
								d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z"
								clip-rule="evenodd"
							/>
						</svg>
						<span
							><strong class="font-semibold text-gray-900">Barbecuing.</strong> Experimenting with
							new recipies. <span class="text-xl">🔬</span></span
						>
					</li>
				</ul>

				<hr class="my-8 border-t-2 border-slate-300" />

				<h2 class="space-grotesk mt-8 text-2xl font-bold tracking-tight text-gray-900">
	
				<div class="flex justify-start">
					<Accordion type="single" collapsible>
						<AccordionItem value="goals" class="border-none">
							<AccordionTrigger class="w-fit  [&>svg]:hidden ">
								<Button
									text={'English Goals'}
									disableLink={true}
									bgColor={'hsl(227, 66%, 55%)'}
									bgDepthColor={'hsl(227, 66%, 25%)'}
								/>
							</AccordionTrigger>
							<AccordionContent
								class="mt-2 rounded-md border-[3px] border-dashed border-indigo-400 p-4"
							>
							<p class="my-4 text-lg font-medium text-black">
								I set myself the challenge of watching the entire <span class="font-bold text-indigo-500">Pirates of the Caribbean</span> saga in English to improve my listening skills understanding.  
								With all its movies combined, it was the perfect adventure to dive into the language.  
								<span class="font-bold text-indigo-500">Challenge Accepted. 🏴‍☠️</span>
							</p>
							
								<ul class="space-y-2">
									{#each goals as { icon, text }}
										<li class="mt-2 flex items-center gap-2 text-lg">
											<span>{icon}</span>
											<span>{text}</span>
										</li>
									{/each}
								</ul>
							</AccordionContent>
						</AccordionItem>
					</Accordion>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Caveat:wght@400;500&family=Roboto+Mono&family=Roboto:wght@400;900&family=Space+Grotesk:wght@500&display=swap');

	.wave {
		animation-name: wave-animation;
		animation-duration: 3s;
		animation-iteration-count: 1;
		transform-origin: 70% 70%;
		display: inline-block;
	}

	@keyframes wave-animation {
		0% {
			transform: rotate(0deg);
		}
		10% {
			transform: rotate(14deg);
		} /* The following five values can be played with to make the waving more or less extreme */
		20% {
			transform: rotate(-8deg);
		}
		30% {
			transform: rotate(14deg);
		}
		40% {
			transform: rotate(-4deg);
		}
		50% {
			transform: rotate(10deg);
		}
		60% {
			transform: rotate(0deg);
		} /* Reset for the last half to pause */
		100% {
			transform: rotate(0deg);
		}
	}
</style>
