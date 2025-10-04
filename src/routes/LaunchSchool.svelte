<script lang="ts">
	import Button from '$lib/components/Button.svelte';
	let isHoveredLS: boolean = false;
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<!-- svelte-ignore a11y-mouse-events-have-key-events -->
<div class="mx-auto max-w-7xl py-12 px-4 sm:py-16 sm:px-6 lg:px-8 lg:py-24">
	<img src="logo-cor.png" class="mx-auto w-3/4 md:w-1/3 my-4" alt="" />
	<div class="mx-auto max-w-4xl text-center">
		<h2 class="text-3xl font-bold tracking-tight text-white sm:text-4xl glow-red space-grotesk">
			Core Curriculum Graduate
		</h2>
	</div>
	<dl class="mt-10 text-center sm:mx-auto sm:grid sm:max-w-3xl sm:grid-cols-3 sm:gap-8">
		<div class="flex flex-col">
			<dt class="order-2 mt-2 text-lg font-medium leading-6 text-red-400">Months</dt>
			<dd class="order-1 text-5xl font-bold tracking-tight text-red-50 glow-red">60</dd>
		</div>
		<div class="mt-10 flex flex-col sm:mt-0">
			<dt class="order-2 mt-2 text-lg font-medium leading-6 text-red-400">Study Hours</dt>
			<dd class="order-1 text-5xl font-bold tracking-tight text-red-50 glow-red">30000</dd>
		</div>
		<div class="mt-10 flex flex-col sm:mt-0">
			<dt class="order-2 mt-2 text-lg font-medium leading-6 text-red-400">Assessments</dt>
			<dd class="order-1 text-5xl font-bold tracking-tight text-red-50 glow-red">150</dd>
		</div>
	</dl>

	<!-- Reflection on LS -->
	<div
		on:mouseover={() => (isHoveredLS = true)}
		on:mouseout={() => (isHoveredLS = false)}
		class="bg-white mt-8 lg:mx-48 px-6 py-8 rounded-md bg-gradient-to-b from-neutral-100 to-neutral-300 hover:outline-dotted hover:outline-4 outline-red-400 outline-offset-4 glow-box-red"
	>
		<h2 class="mt-4 text-2xl font-bold tracking-tight text-gray-900 space-grotesk">
			Notes on University of Cordoba
		</h2>
		<p class="my-6 text-gray-600">
			My time at the University of Córdoba has been one of the greatest challenges I've ever faced,
			 but also one of the most enriching experiences. Beyond learning theory 
			and technical concepts, I developed a keen attention to detail and methodical thinking.
			<br /><br />
			Academic training begins with fundamental principles, which isn't always the easiest way to begin, 
			but it reflects the seriousness of the program. A thorough understanding of the foundations is a 
			requirement before moving on to more complex levels, and that's precisely 
			what makes the university training experience so valuable.
			<span class="text-xl" class:hithere={isHoveredLS}>🎉</span>
		</p>
		<Button
			text={'View Curriculum'}
			href={'https://www.unicordoba.edu.co/'}
			targetBlank={true}
			bgColor={'hsl(349, 98%, 58%)'}
			bgDepthColor={'hsl(340, 97%, 38%)'}
		/>
	</div>
</div>
