<script lang="ts">
	import Product from '$lib/components/product.svelte';

	const air_mailer_icons = [
		{ linkURL: 'https://www.typescriptlang.org/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg' },
		{ linkURL: 'https://svelte.dev/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/svelte/svelte-original.svg' },
		{ linkURL: 'https://nodejs.org/en', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg' },
		{ linkURL: 'https://en.wikipedia.org/wiki/MongoDB', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg' },
		{ linkURL: 'https://firebase.google.com/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg' },
		{ linkURL: 'https://tailwindcss.com/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg' },
		{ linkURL: 'https://stripe.com/', imgURL: 'https://www.solodev.com/file/2e7ff4de-48b3-11ed-bb2e-0eaef3759f5f/stripe-icon.png' }
	];

	const data_forest_icons = [
		{ linkURL: 'https://www.typescriptlang.org/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg' },
		{ linkURL: 'https://svelte.dev/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/svelte/svelte-original.svg' },
		{ linkURL: 'https://nodejs.org/en', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg' },
		{ linkURL: 'https://en.wikipedia.org/wiki/MongoDB', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg' },
		{ linkURL: 'https://firebase.google.com/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg' },
		{ linkURL: 'https://tailwindcss.com/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg' }
	];

	const vertical_spanish_icons = [
		{ linkURL: 'https://en.wikipedia.org/wiki/JavaScript', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg' },
		{ linkURL: 'https://svelte.dev/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/svelte/svelte-original.svg' },
		{ linkURL: 'https://nodejs.org/en', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg' },
		{ linkURL: 'https://en.wikipedia.org/wiki/MongoDB', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg' },
		{ linkURL: 'https://tailwindcss.com/', imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg' },
		{ linkURL: 'https://www.algolia.com/', imgURL: 'https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/12_Algolia_logo_logos-512.png' },
		{ linkURL: 'https://www.contentful.com/', imgURL: 'contentful.png' }
	];
</script>

<div id="products" class="bg-slate-950 py-24 sm:py-32">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="mx-auto max-w-2xl text-center">
			<h2 class="text-3xl font-bold tracking-tight sm:text-4xl bg-gradient-to-r text-indigo-300 glow">Public Products</h2>
			<p class="mt-2 text-lg leading-8 text-gray-400">Here are a few of public facing products that I have worked on.</p>
		</div>

		<!-- Products -->
		<div class="mx-auto mt-16 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-3">
			<Product
				category="Mailing Lists"
				title="AirMailer.io"
				description="AirMailer.io allows marketers to generate mailing list with a little as an address. I like to think of it as a vending machine for aparment mailing lists."
				linkURL="https://airmailer.io"
				imgURL="airmailer_ss.png"
				icons={air_mailer_icons}
			/>

			<Product
				category="Homeowner Data"
				title="DataForest.io"
				description="DataForest.io allows marketers to market geotarget homeowners. Think, Google Maps for homeowner + propery data."
				linkURL="https://dataforest.io"
				imgURL="dataforest_ss.png"
				icons={data_forest_icons}
			/>

			<Product
				category="Language Learning"
				title="VerticalSpanish.com"
				description="Vertical Spanish allows Spanish students to study spanish verbs in a world that inspires. Conjugators are notorious for being overpopulated with ads, but not here!"
				linkURL="https://verticalspanish.com"
				imgURL="landscape.png"
				icons={vertical_spanish_icons}
			/>
		</div>
	</div>
</div>
