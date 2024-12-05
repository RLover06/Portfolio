<script lang="ts">
	import { onMount } from 'svelte';
	import Header from './Header.svelte';
	import Hero from './Hero.svelte';
	import Letter from './Letter.svelte';
	import TechStack from './TechStack.svelte';
	import Products from './Products.svelte';
	import LaunchSchool from './LaunchSchool.svelte';
	import Contact from './Contact.svelte';
	import Favorites from './Favorites.svelte';
	import Footer from './Footer.svelte';
	import Testimonials from './Testimonials.svelte';
	import OpenSource from '$lib/components/OpenSource.svelte';

	let ready = false;

	onMount(() => {
		ready = true;
	});
</script>

{#if ready}
	<Header />
	<Hero />
	<Testimonials />
	<Letter />
	<TechStack />
	<OpenSource />
	<Products />
	<LaunchSchool />
	<Contact />
	<Favorites />
	<Footer />
{/if}
