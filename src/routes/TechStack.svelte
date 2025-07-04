<script lang="ts">
	import Icon from '$lib/components/Icon.svelte';
	import { animate, stagger, inView } from 'motion';
	import { onMount } from 'svelte';

	const technologies = [
		{
			name: 'TypeScript',
			linkURL: 'https://www.typescriptlang.org/',
			imgURL:
				'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg',
		},
		{
			name: 'JavaScript',
			linkURL: 'https://en.wikipedia.org/wiki/JavaScript',
			imgURL:
				'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg',
		},
		{
			name: 'Node.js',
			linkURL: 'https://nodejs.org/en',
			imgURL: 'node.png',
		},
		{
			name: 'Bun',
			linkURL: 'https://bun.sh',
			imgURL: 'bun.svg',
		},
		{
			name: 'Svelte',
			linkURL: 'https://svelte.dev/',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/svelte/svelte-original.svg',
		},
		{
			name: 'React',
			linkURL: 'https://react.dev/',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg',
		},
		{
			name: 'Alpine.js',
			linkURL: 'https://alpinejs.dev/',
			imgURL: 'alpine.png',
		},
		{
			name: 'Next.js',
			linkURL: 'https://nextjs.org/',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg',
		},
		{
			name: 'Astro',
			linkURL: 'https://astro.build/',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/astro/astro-original.svg',
		},
		{
			name: 'Vite.js',
			linkURL: 'https://vitejs.dev/',
			imgURL: 'vite.png',
		},
		{
			name: 'Supabase',
			linkURL: 'https://supabase.com/',
			imgURL: 'supabase.png',
		},
		{
			name: 'MongoDB',
			linkURL: 'https://www.mongodb.com/',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg',
		},
		{
			name: 'Firebase',
			linkURL: 'https://firebase.google.com/',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg',
		},
		{
			name: 'Pinecone',
			linkURL: 'https://pinecone.io',
			imgURL: 'https://yepcode.io/docs/img/integrations/icons/pinecone.svg',
		},
		{
			name: 'Prisma',
			linkURL: 'https://www.prisma.io/',
			imgURL: 'prisma.png',
		},
		{
			name: 'Drizzle',
			linkURL: 'https://www.drizzle.team/',
			imgURL: 'drizzle.png',
		},
		{
			name: 'Postgres',
			linkURL: 'https://www.postgresql.org/',
			imgURL:
				'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg',
		},
		{
			name: 'MySQL',
			linkURL: 'https://www.mysql.com/',
			imgURL: 'mysql.png',
		},
		{
			name: 'HTML',
			linkURL: 'https://en.wikipedia.org/wiki/HTML5',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg',
		},
		{
			name: 'CSS',
			linkURL: 'https://developer.mozilla.org/en-US/docs/Web/CSS',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg',
		},
		{
			name: 'Tailwind CSS',
			linkURL: 'https://tailwindcss.com/',
			imgURL:
				'https://raw.githubusercontent.com/devicons/devicon/6910f0503efdd315c8f9b858234310c06e04d9c0/icons/tailwindcss/tailwindcss-original.svg',
		},
		{
			name: 'Shadcn UI',
			linkURL: 'https://ui.shadcn.com/',
			imgURL: 'shadcn-ui.png',
		},
		{
			name: 'Daisy UI',
			linkURL: 'https://daisyui.com/',
			imgURL: 'daisy-ui.png',
		},
		{
			name: 'Vitest',
			linkURL: 'https://vitest.dev/',
			imgURL: 'vite-test.png',
		},
		{
			name: 'Playwright',
			linkURL: 'https://playwright.dev/',
			imgURL: 'playwright.webp',
		},
		{
			name: 'Jest',
			linkURL: 'https://jestjs.io/',
			imgURL: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jest/jest-plain.svg',
		},
		{
			name: 'Docker',
			linkURL: 'https://docker.com/',
			imgURL: 'docker.png',
		},
		{
			name: 'Vercel',
			linkURL: 'https://vercel.com/',
			imgURL: 'vercel.png',
		},
		{
			name: 'Netlify',
			linkURL: 'https://www.netlify.com/',
			imgURL: 'netlify.png',
		},
		{
			name: 'Google Cloud Platform',
			linkURL: 'https://cloud.google.com/',
			imgURL:
				'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/googlecloud/googlecloud-original.svg',
		},
		{
			name: 'Mapbox',
			linkURL: 'https://www.mapbox.com/',
			imgURL: 'mapbox.png',
		},
		{
			name: 'Stripe',
			linkURL: 'https://stripe.com/',
			imgURL: 'https://www.solodev.com/file/2e7ff4de-48b3-11ed-bb2e-0eaef3759f5f/stripe-icon.png',
		},
		{
			name: 'Cloudinary',
			linkURL: 'https://cloudinary.com/',
			imgURL: 'cloudinary.png',
		},
		{
			name: 'Replicate',
			linkURL: 'https://replicate.com',
			imgURL: 'replicate.jpg',
		},
		{
			name: 'Algolia',
			linkURL: 'https://www.algolia.com/',
			imgURL:
				'https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/12_Algolia_logo_logos-512.png',
		},
		{
			name: 'Google Drive API',
			linkURL: 'https://developers.google.com/drive/api/guides/about-sdk',
			imgURL: 'google-drive.png',
		},
		{
			name: 'Contentful',
			linkURL: 'https://www.contentful.com/',
			imgURL: 'contentful.png',
		},
		{
			name: 'Lucia Auth',
			linkURL: 'https://lucia-auth.com/',
			imgURL: 'lucia.png',
		},
	];

	onMount(() => {
		inView('#tech-icons-end', () => {
			animate('li', { opacity: 1, y: [30, 0] }, { delay: stagger(0.02) });
		});
	});
</script>

<div class="mt-44 pb-1 pt-4" id="tech">
	<div class="">
		<h2
			class="glow space-grotesk bg-gradient-to-r text-center text-3xl font-bold tracking-tight text-indigo-300 sm:text-4xl"
		>
			Technologies Used
		</h2>
		<div class="mx-auto max-w-7xl px-4 py-12 sm:px-6 lg:px-8">
			<ul id="tech-icons" class="grid grid-cols-4 gap-8 md:grid-cols-6 lg:grid-cols-8">
				{#each technologies as tech}
					<li class="tech-icon">
						<Icon name={tech.name} linkURL={tech.linkURL} imgURL={tech.imgURL} />
					</li>
				{/each}
			</ul>
		</div>
		<div id="tech-icons-end"></div>
	</div>
</div>
