<script lang="ts">
	let isHovered: boolean = false;
</script>

<div
	on:mouseover={() => (isHovered = true)}
	on:mouseout={() => (isHovered = false)}
	on:focus={() => (isHovered = true)}
	on:blur={() => (isHovered = false)}
	class="mx-2 p-6 md:mx-48 py-32 my-16 lg:px-8 text-left rounded-md bg-gradient-to-b from-neutral-100 to-neutral-300 object-cover hover:outline-dotted hover:outline-4 outline-indigo-400 outline-offset-4 glow-box"
>
	<div class="mx-auto max-w-3xl text-base leading-7 text-gray-700">
		<p class="text-base font-semibold leading-7 text-indigo-600">Bio</p>
		<h1 class="mt-2 text-3xl font-bold tracking-tight text-gray-700 sm:text-4xl space-grotesk">Hey there! <span class:wave={isHovered}>👋</span></h1>
		<p class="mt-6 text-xl leading-8 font-semibold">
			I am Hunter, from The Woodlands, Texas - just north of Houston. As a full-stack developer, I enjoy building applications of all kinds with people from all over the world.
		</p>
		<div class="mt-10 max-w-2xl text-lg font-medium">
			<div>
				<p>
					I am a huge fan of <span class="font-bold text-black text-lg">JavaScript</span>, and more recently,
					<span class="font-bold text-black text-lg"> TypeScript</span>. The tooling is fantastic but, TypeScript's real magic lies in its ability to make us more conscious about the code we write.

					<br /><br />

					As far as frameworks go, <span class="font-bold text-black text-lg">Svelte</span> is always my first choice. The developer experience is excellent and it’s a dream to use. I am also a huge fan of Rich Harris and
					everything he is doing to push the framework forward.
				</p>

				<br />

				<p>The runner-up goes to <span class="font-bold text-black text-lg">React</span>. Its strong community and ecosystem are something I highly value.</p>
				<br />

				I discovered <span class="font-bold text-black text-lg">Tailwind CSS</span> in 2019 and have been exclusively using it ever since. Lately, I have started using
				<span class="font-bold text-black text-lg">Shadcn UI</span>, the Tailwind-based component library and it's gradually turning into one of my favorites.

				<ul class="mt-16 max-w-2xl space-y-2 text-gray-600">
					<h2 class="mx-auto my-8 text-2xl font-bold tracking-tight text-gray-900 space-grotesk">The <span class="underline decoration-wavy decoration-indigo-600 underline-offset-8">perfect</span> day looks like...</h2>
					<li class="flex gap-x-3">
						<svg class="mt-1 h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
							<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z" clip-rule="evenodd" />
						</svg>
						<span><strong class="font-semibold text-gray-900">Programming.</strong> Building applications gives me energy. <span class="text-xl">⚡️</span></span>
					</li>
					<li class="flex gap-x-3">
						<svg class="mt-1 h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
							<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z" clip-rule="evenodd" />
						</svg>
						<span><strong class="font-semibold text-gray-900">Reading in Spanish.</strong> Best way to improve overall comprehension. <span class="text-xl">📈</span></span>
					</li>
					<li class="flex gap-x-3">
						<svg class="mt-1 h-5 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
							<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0 00-1.214-.882l-3.483 4.79-1.88-1.88a.75.75 0 10-1.06 1.061l2.5 2.5a.75.75 0 001.137-.089l4-5.5z" clip-rule="evenodd" />
						</svg>
						<span><strong class="font-semibold text-gray-900">Barbecuing.</strong> Experimenting with new recipies. <span class="text-xl">🔬</span></span>
					</li>
				</ul>

				<h2 class="mt-16 text-2xl font-bold tracking-tight text-gray-900 space-grotesk">Notes on Spanish</h2>
				<p class="mt-6">
					The Spanish language has been many things to me. It has been a teacher, teaching me <span class="caveat text-2xl font-bold text-indigo-500">dedication</span>,
					<span class="caveat text-2xl font-bold text-indigo-500">patience</span>, and <span class="caveat text-2xl font-bold text-indigo-500">discipline</span>. It has also been a vehicle for self-confidence. And after
					non-stop intense study, Spanish is now a part of my identity. I've spent the last
					<span class="font-bold">5 years</span>
					living among the Latino community, taking the opportunity to listen, learn and eventually gain a deep understanding. <br /><br /> I've integrated many positive aspects of the Latin American lifestyle into my
					own life, with the most important lesson at the top of mind -
					<strong class="bg-gradient-to-b from-pink-600 via-red-600 to-fuchsia-700 text-transparent bg-clip-text font-black text-xl">Love life</strong>
					<span class="p-2 text-xl">❤️</span>
					<br /><br />
					<span class="text-indigo-600 font-bold italic"
						>Currently - B2
						<span class="mx-4 text-indigo-600 font-bold italic">
							Goal - C1
							<span class="text-slate-500">(Dec. 2024)</span>
						</span>
					</span>
				</p>
			</div>
		</div>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Caveat:wght@400;500&family=Roboto+Mono&family=Roboto:wght@400;900&family=Space+Grotesk:wght@500&display=swap');

	.hovered-font {
		font-family: 'Caveat', serif;
	}

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

	.gelatine {
		display: inline-block;
		animation: gelatine 1s;
		animation-iteration-count: 5;
	}

	@keyframes gelatine {
		0% {
			transform: scale(1, 1);
		}
		25% {
			transform: scale(0.9, 1.1);
		}
		50% {
			transform: scale(1.1, 0.9);
		}
		75% {
			transform: scale(0.95, 1.05);
		}
	}
</style>
