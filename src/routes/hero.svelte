<script lang="ts">
	import { blur } from 'svelte/transition';

	let image = '/hunter-coco.jpg';
</script>

<div class="mt-10 mx-auto max-w-screen-xl px-2 sm:px-6 md:mt-16 lg:mt-20 xl:mt-28">
	<div class="text-center">
		<div transition:blur={{ duration: 1500 }} class="image-wrapper relative w-3/4 md:w-1/3 h-auto mx-auto p-4 rounded-full group">
			<img src="/headshot.jpeg" alt="" class="h-full w-full object-cover rounded-full glow-box group-hover:hidden" />
			<img src="/hunter-coco.jpg" alt="" class="h-full w-full object-cover rounded-full glow-box hidden group-hover:block" />
		</div>

		

		<h2 transition:blur={{ duration: 2000 }} class="mt-10 text-4xl tracking-tight leading-10 font-extrabold text-gray-100 sm:text-5xl sm:leading-none md:text-6xl drop-shadow-lg glow space-grotesk">
			Hunter Stevens
			<br />
			<span transition:blur={{ duration: 3000 }} class="whitespace-nowrap bg-gradient-to-r text-indigo-300 space-grotesk">Software Developer</span>
		</h2>

		<div class="mt-3 max-w-md mx-auto text-base text-neutral-600 sm:text-xl md:mt-5 md:text-xl md:max-w-3xl">
			<div transition:blur={{ duration: 3500 }} class="flex justify-center gap-2">
				<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M4.26 10.147a60.438 60.438 0 0 0-.491 6.347A48.62 48.62 0 0 1 12 20.904a48.62 48.62 0 0 1 8.232-4.41 60.46 60.46 0 0 0-.491-6.347m-15.482 0a50.636 50.636 0 0 0-2.658-.813A59.906 59.906 0 0 1 12 3.493a59.903 59.903 0 0 1 10.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.717 50.717 0 0 1 12 13.489a50.702 50.702 0 0 1 7.74-3.342M6.75 15a.75.75 0 1 0 0-1.5.75.75 0 0 0 0 1.5Zm0 0v-3.675A55.378 55.378 0 0 1 12 8.443m-7.007 11.55A5.981 5.981 0 0 0 6.75 15.75v-1.5"
					/>
				</svg>
				<a href="https://www.uh.edu/" target="_blank">
					<span class="font-semibold bg-gradient-to-b from-slate-100 via-neutral-300 to-slate-600 text-transparent bg-clip-text"> University of Houston <span class="hidden md:inline">(BBA in Marketing)</span> </span>
				</a>
				<br />
			</div>

			<div transition:blur={{ duration: 4000 }} class="flex justify-center gap-2">
				<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M9 12.75 11.25 15 15 9.75M21 12c0 1.268-.63 2.39-1.593 3.068a3.745 3.745 0 0 1-1.043 3.296 3.745 3.745 0 0 1-3.296 1.043A3.745 3.745 0 0 1 12 21c-1.268 0-2.39-.63-3.068-1.593a3.746 3.746 0 0 1-3.296-1.043 3.745 3.745 0 0 1-1.043-3.296A3.745 3.745 0 0 1 3 12c0-1.268.63-2.39 1.593-3.068a3.745 3.745 0 0 1 1.043-3.296 3.746 3.746 0 0 1 3.296-1.043A3.746 3.746 0 0 1 12 3c1.268 0 2.39.63 3.068 1.593a3.746 3.746 0 0 1 3.296 1.043 3.746 3.746 0 0 1 1.043 3.296A3.745 3.745 0 0 1 21 12Z"
					/>
				</svg>
				<a href="https://launchschool.com/courses" target="_blank">
					<span class="font-semibold bg-gradient-to-b from-slate-100 via-neutral-300 to-slate-600 text-transparent bg-clip-text">
						Launch School <span class="hidden md:inline">(Core Curriculum)</span>
					</span>
				</a>
			</div>

			<div transition:blur={{ duration: 4500 }} class="flex justify-center gap-2">
				<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M21.75 6.75a4.5 4.5 0 0 1-4.884 4.484c-1.076-.091-2.264.071-2.95.904l-7.152 8.684a2.548 2.548 0 1 1-3.586-3.586l8.684-7.152c.833-.686.995-1.874.904-2.95a4.5 4.5 0 0 1 6.336-4.486l-3.276 3.276a3.004 3.004 0 0 0 2.25 2.25l3.276-3.276c.256.565.398 1.192.398 1.852Z"
					/>
					<path stroke-linecap="round" stroke-linejoin="round" d="M4.867 19.125h.008v.008h-.008v-.008Z" />
				</svg>
				<a href="https://www.mlytica.com/" target="_blank">
					<span class="font-semibold bg-gradient-to-b from-slate-100 via-neutral-300 to-slate-600 text-transparent bg-clip-text">Software Dev @ MLytica</span>
				</a>
			</div>
		</div>
	</div>
</div>

<!-- Certifications -->
<!-- <div transition:blur={{ duration: 5500 }} class="flex w-1/2 mx-auto justify-between my-10 px-24">
  <img class="size-32 shake-on-hover" src="logo-aws-cp.png" alt="">
  <img class="size-32 shake-on-hover" src="logo-aws-sa.png" alt="">
  <img class="size-32 shake-on-hover" src="logo-aws-d.png" alt="">
</div> -->
