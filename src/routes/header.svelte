<script>
	import { blur } from 'svelte/transition';
	import Button from '$lib/components/button.svelte';

	let mobileOpen = false;
</script>

<nav class="m-4 relative flex items-center justify-between sm:h-10 md:justify-center">
	<div transition:blur={{ duration: 2000 }} class="flex items-center flex-1 md:absolute md:inset-y-0 md:left-0">
		<div class="flex items-center justify-between w-full md:w-auto">
			<div class="-mr-2 flex items-center md:hidden">
				<button
					on:click={() => (mobileOpen = !mobileOpen)}
					type="button"
					class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-200 focus:outline-none focus:bg-gray-200 focus:text-gray-500 transition duration-150 ease-in-out"
				/>
			</div>
		</div>

		<ul class="flex rounded-full bg-white/90 px-3 text-sm text-indigo-500 font-bold shadow-lg shadow-zinc-800/5 ring-1 ring-zinc-900/5 backdrop-blur dark:bg-zinc-800/90 dark:text-zinc-200 dark:ring-white/10">
			<li class="relative flex items-center px-3 py-2 transition hover:text-indigo-700">Native: <span class="text-xl mx-1">🇺🇸</span></li>
			<li class="relative flex items-center px-3 py-2 transition hover:text-indigo-700">C1: <span class="text-xl mx-1">🇪🇸</span></li>
		</ul>
	</div>

	<nav class="pointer-events-auto hidden md:block">
		<ul class="flex rounded-full bg-white/90 px-3 text-sm text-indigo-500 font-bold shadow-lg shadow-zinc-800/5 ring-1 ring-zinc-900/5 backdrop-blur dark:bg-zinc-800/90 dark:text-zinc-200 dark:ring-white/10">
			<li><a class="relative block px-3 py-2 transition hover:text-indigo-700" href="#tech">Technologies</a></li>
			<li><a class="relative block px-3 py-2 transition hover:text-indigo-700" href="#products">Products</a></li>
			<li><a class="relative block px-3 py-2 transition hover:text-indigo-700" href="#contact">Contact</a></li>
			<li><a class="relative block px-3 py-2 transition hover:text-indigo-700" href="#favorites">Favorites</a></li>
		</ul>
	</nav>

	<div transition:blur={{ duration: 2000 }} class="hidden md:absolute md:flex md:items-center md:justify-end md:inset-y-0 md:right-0">
		<a href="https://github.com/diamondalltheway" target="_blank" class="ml-6 text-gray-600 hover:text-gray-700">
			<svg class="h-10 w-10 mx-6 text-indigo-500 bg-indigo-200 rounded-full" fill="currentColor" viewBox="0 0 24 24">
				<path
					fill-rule="evenodd"
					d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"
					clip-rule="evenodd"
				/>
			</svg>
		</a>
		<span class="inline-flex rounded-md">
			<Button text={'Contact'} href={'#contact'} targetBlank={false} bgColor={'hsl(227, 66%, 55%)'} bgDepthColor={'hsl(227, 66%, 25%)'} />
		</span>
	</div>
</nav>
