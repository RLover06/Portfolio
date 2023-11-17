<script>
	import { blur } from 'svelte/transition';
</script>

<div class="mt-10 mx-auto max-w-screen-xl px-2 sm:px-6 md:mt-16 lg:mt-20 xl:mt-28">
	<div class="text-center">
		<div transition:blur={{ duration: 1500 }} class="image-wrapper relative w-3/4 md:w-1/3 h-auto mx-auto p-4 rounded-full">
			<img src="/headshot.jpeg" alt="" class="h-full w-full object-cover rounded-full glow-box" />
		</div>

		<h2 transition:blur={{ duration: 2000 }} class="mt-10 text-4xl tracking-tight leading-10 font-extrabold text-gray-100 sm:text-5xl sm:leading-none md:text-6xl drop-shadow-lg glow">
			Hunter Stevens
			<br />
			<span transition:blur={{ duration: 3000 }} class="whitespace-nowrap bg-gradient-to-r text-indigo-300">Full-Stack Developer</span>
		</h2>

		<div class="mt-3 max-w-md mx-auto text-base text-gray-400 sm:text-xl md:mt-5 md:text-xl md:max-w-3xl">
			<div transition:blur={{ duration: 3500 }}>
				Education:
				<a href="https://launchschool.com/courses" target="_blank">
					<span class="font-semibold text-green-300 italic"> University of Houston <span class="hidden md:inline">(BBA in Marketing)</span> </span>
				</a>
				<br />
			</div>

			<div transition:blur={{ duration: 4000 }}>
				Certifications:
				<a href="https://launchschool.com/courses" target="_blank">
					<span class="font-semibold text-green-300 italic">
						Launch School <span class="hidden md:inline">(Core Curriculum)</span>
					</span>
				</a>
			</div>

			<div transition:blur={{ duration: 4500 }}>
				Building: <span class="font-semibold text-green-300 italic">DataForest.io</span>
			</div>

			<div transition:blur={{ duration: 5000 }}>
				Learning: <span class="font-semibold text-green-300">Playwright</span>
			</div>
		</div>
	</div>
</div>
