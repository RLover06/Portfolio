<script lang="ts">
	import { onMount } from 'svelte';
	import { blur } from 'svelte/transition';
	import VideoIcon from '$lib/svgs/Video.svelte';
	import BadgeIcon from '$lib/svgs/Badge.svelte';
	import GraduationIcon from '$lib/svgs/Graduation.svelte';
	import WordsFadeIn from '$lib/components/WordsFadePullUp.svelte';
	import AnimatedShinyText from '$lib/components/AnimatedShinyText.svelte';
	let image = '/hunter-coco.jpg';
	let primaryTitleIsReady = false;
	let secondaryTitleIsReady = false;

	onMount(() => {
		setTimeout(() => {
			primaryTitleIsReady = true;
		}, 500);
		setTimeout(() => {
			secondaryTitleIsReady = true;
		}, 1200);
	});
</script>

<div class="mx-auto max-w-screen-xl px-2 sm:px-6 md:mt-16 h-screen">
	<div class="text-center">
		<div
			transition:blur={{ delay: 200, duration: 600 }}
			class="image-wrapper relative w-3/4 md:w-1/3 h-auto mx-auto p-4 rounded-full group"
		>
			<img
				src="/headshot.jpeg"
				alt=""
				class="h-full w-full object-cover rounded-full glow-box group-hover:hidden"
			/>
			<img
				src="/hunter-coco.jpg"
				alt=""
				class="h-full w-full object-cover rounded-full glow-box hidden group-hover:block"
			/>
		</div>

		{#if primaryTitleIsReady}
			<WordsFadeIn words="Hunter Stevens" class="mt-6 text-4xl tracking-tight leading-10 font-extrabold text-gray-100 sm:text-5xl sm:leading-none md:text-6xl drop-shadow-lg glow space-grotesk" />
		{/if}

		{#if secondaryTitleIsReady}
			<WordsFadeIn 
				words="Software Developer" 
				class="mt-2 text-4xl tracking-tight leading-10 font-extrabold text-gray-100 sm:text-5xl sm:leading-none md:text-6xl drop-shadow-lg glow space-grotesk"
			/>
		{/if}

		<div
			class="mt-3 max-w-md mx-auto text-base text-neutral-600 sm:text-xl md:mt-5 md:text-xl md:max-w-3xl"
		>
			<div transition:blur={{ delay: 1500, duration: 500 }} class="flex justify-center gap-2">
				<GraduationIcon />
				<a href="https://www.uh.edu/" target="_blank">
					<span
						class="font-semibold bg-gradient-to-b from-slate-100 via-neutral-300 to-slate-600 text-transparent bg-clip-text"
					>
						University of Houston <span class="hidden md:inline">(BBA in Marketing)</span>
					</span>
				</a>
				<br />
			</div>

			<div transition:blur={{ delay: 2000, duration: 500 }} class="flex justify-center gap-2">
				<BadgeIcon />
				<a href="https://launchschool.com/courses" target="_blank">
					<span
						class="font-semibold bg-gradient-to-b from-slate-100 via-neutral-300 to-slate-600 text-transparent bg-clip-text"
					>
						Launch School <span class="hidden md:inline">(Core Curriculum Grad)</span>
					</span>
				</a>
			</div>

			<div transition:blur={{ delay: 2500, duration: 500 }} class="flex justify-center gap-2 items-center">
				<VideoIcon />
				<div class="flex gap-2 items-center">
					<a
						href="https://www.youtube.com/@HunterScript/featured"
						class="px-1.5 -py-1 bg-white/20 rounded-xl border-2 border-gray-700 hover:bg-white/10"
					>
						<button
							class="font-semibold bg-gradient-to-b from-slate-100 via-neutral-300 to-slate-600 text-transparent bg-clip-text"
						>
							@HunterScript
						</button>
					</a>
				</div>
			</div>
		</div>
	</div>
</div>

<!-- Certifications -->
<!-- <div transition:blur={{ duration: 5500 }} class="flex w-1/2 mx-auto justify-between my-10 px-24">
  <img class="size-32 hover:motion-preset-shake" src="logo-aws-cp.png" alt="">
  <img class="size-32 hover:motion-preset-shake" src="logo-aws-sa.png" alt="">
  <img class="size-32 hover:motion-preset-shake" src="logo-aws-d.png" alt="">
</div> -->
