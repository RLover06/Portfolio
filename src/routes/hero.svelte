<script lang="ts">
	import { onMount } from 'svelte';
	import { blur } from 'svelte/transition';
	import VideoIcon from '$lib/svgs/Video.svelte';
	import BadgeIcon from '$lib/svgs/Badge.svelte';
	import GraduationIcon from '$lib/svgs/Graduation.svelte';
	import WordsFadeIn from '$lib/components/WordsFadePullUp.svelte';
	// import AnimatedShinyText from '$lib/components/AnimatedShinyText.svelte';
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
		<div class="relative w-3/4 md:w-1/3 aspect-square mx-auto group">
			<div 
				transition:blur={{ delay: 200, duration: 600 }}
				class="absolute inset-0 image-wrapper group-hover:opacity-0 transition-opacity duration-300"
			>
				<div class="absolute inset-3 rounded-full overflow-hidden">
					<img
						src="/headshot.jpeg"
						alt=""
						class="w-full h-full object-cover"
					/>
				</div>
			</div>

			<div 
				transition:blur={{ delay: 200, duration: 600 }}
				class="absolute inset-0 image-wrapper opacity-0 group-hover:opacity-100 transition-opacity duration-300"
			>
				<div class="absolute inset-3 rounded-full overflow-hidden">
					<img
						src="/hunter-coco.jpg"
						alt=""
						class="w-full h-full object-cover"
					/>
				</div>
			</div>
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
						class="px-1.5 -py-1 rounded-xl bg-white/10 hover:bg-white/20"
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

<style>
	.image-wrapper::before {
		content: '';
		position: absolute;
		top: -2px; /* Adjust based on desired offset */
		left: -2px; /* Adjust based on desired offset */
		width: calc(100% + 4px); /* Adjust based on desired offset */
		height: calc(100% + 4px); /* Adjust based on desired offset */
		border: 4px dashed #aaabef;
		border-radius: 50%;
		animation: spin 100s linear infinite;
	}

.image-wrapper img {
	position: relative;
	z-index: 1;
}
</style>