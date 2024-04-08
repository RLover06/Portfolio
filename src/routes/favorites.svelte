<script lang="ts">
	import * as Accordion from '$lib/components/ui/accordion';
	import Favorite from '$lib/components/favorite.svelte';

	const books = [
		{ col_1: 'The Little Prince', col_2: 'Antoine de Saint-Exupéry' },
		{ col_1: '12 Rules for Life', col_2: 'Jordan B. Peterson' },
		{ col_1: 'Hard Thing About Hard Things', col_2: 'Ben Horowitz' },
		{ col_1: 'Zero to One', col_2: 'Peter Thiel' },
		{ col_1: 'Rework', col_2: 'Jason Fried • David Heinemeier Hanson' },
		{ col_1: 'Delivering Happiness', col_2: 'Tony Hsieh' },
		{ col_1: 'The Launch Pad: Inside Y Combinator', col_2: 'Randal Stross' },
		{ col_1: 'Remote', col_2: 'Jason Fried • David Heinemeier Hanson' },
		{ col_1: 'Shoe Dog', col_2: 'Phil Knight' },
		{ col_1: 'Crazy Love', col_2: 'Francis Chan' },
		{ col_1: 'Tocqueville and the American Experiment', col_2: 'William R. Cook' },
		{ col_1: 'Extreme Ownership', col_2: 'Jacko Wilink • Leif Babin' },
		{ col_1: 'Outliers', col_2: 'Malcom Gladwell' },
		{ col_1: 'David and Goliath', col_2: 'Malcom Gladwell' },
		{ col_1: 'A New Grammar Reference of Modern Spanish', col_2: 'John Butt • Carmen Benjamin' }
	];

	const podcasts = [
		{ col_1: 'The Joe Rogan Experience', col_2: 'Great exposure to a little bit of everything' },
		{ col_1: 'Syntax', col_2: 'Endless web dev knowledge' },
		{ col_1: 'Lex Fridman Podcast', col_2: 'Great Tech/Culture discussions' },
		{ col_1: 'This Past Weekend w/ Theo Von', col_2: 'Authentic, funny, gotta love it - gang gang!' },
		{ col_1: 'Huberman Lab', col_2: 'Actionable science' },
		{ col_1: 'You Can Learn Chinese Podcast', col_2: 'Best language learning tips out there!' },
		{ col_1: "Matt & Shane's Secret Podcast", col_2: 'Laughs when I need to relax' },
		{ col_1: 'Podrocket', col_2: 'Great software development opinions' },
		{ col_1: 'No Hay Banderas en Marte', col_2: 'La mejor manera de mejorar mi español' }
	];

	const movies = [
		{ col_1: "You've Got Mail" },
		{ col_1: 'Interstellar' },
		{ col_1: 'Blood Diamond' },
		{ col_1: 'Angels in the Outfield' },
		{ col_1: 'Lord of the Rings (Trilogy)' },
		{ col_1: 'Gangs of New York' },
		{ col_1: '100 Foot Journey' },
		{ col_1: 'The Matrix' },
		{ col_1: 'Training Day' },
		{ col_1: 'Catch Me If You Can' }
	];

	const shows = [
		{ col_1: 'Severance' },
		{ col_1: 'Suits' },
		{ col_1: "That 70's Show" },
		{ col_1: 'Body Guard' },
		{ col_1: 'Line of Duty' },
		{ col_1: 'Dexter' },
		{ col_1: 'Cheers' },
		{ col_1: 'Yu Yu Hakusho' },
		{ col_1: 'True Detective' },
		{ col_1: 'Fargo' }
	];

	const places = [
		{ col_1: 'The Woodlands, Texas', col_2: "I'm a hometown kind of guy" },
		{ col_1: 'Tenerife, Spain', col_2: 'Incredible amount of microclimates' },
		{ col_1: 'Medellín, Colombia', col_2: 'Lived here for 6 years, más paisa que una arepa' },
		{ col_1: 'Denver, Colorado', col_2: 'Lived here for a year, Rocky Mountain Air' },
		{ col_1: 'Papagayo, Costa Rica', col_2: 'Great family memories' },
		{ col_1: 'Rome, Italy', col_2: 'If Rome can fall, nothing is forever' },
		{ col_1: 'Maui, Hawaii', col_2: 'Never been more relaxed' },
		{ col_1: 'Nassau, Bahamas', col_2: 'More fond family memories' },
		{ col_1: 'Cusco, Peru', col_2: 'Ancient' },
		{ col_1: 'Lima, Peru', col_2: 'Ceviche' },
		{ col_1: 'Florence, Italy', col_2: 'Refreshing taste of craftsmanship' },
		{ col_1: 'San Pedro de Atacama, Chile', col_2: 'Surreal landscapes' },
		{ col_1: 'Kauai, Hawaii', col_2: 'Classic family memories' },
		{ col_1: 'Grand Cayman, Cayman Islands', col_2: 'Islands are easy to love' },
		{ col_1: 'Lübbecke, Germany', col_2: 'First taste of Europe' },
		{ col_1: 'Jardín, Colombia', col_2: "Named 'Garden' in Spanish for its beauty" },
		{ col_1: 'Madrid, Spain', col_2: 'All around underrated' },
		{ col_1: 'Granada, Spain', col_2: 'Creativity that inspires' },
		{ col_1: 'Paracas, Perú', col_2: 'Animals all over the place' },
		{ col_1: 'Valle de Corcoa, Colombia', col_2: 'Tallest palm trees in the world' }
	];
</script>

<div class="md:w-3/5 mx-auto text-white">
	<h2 class="text-center text-3xl leading-9 font-extrabold text-green-400 sm:text-4xl sm:leading-10 glow-green">Favorites</h2>
	<Accordion.Root>
		<!-- Books -->
		<Accordion.Item value="books">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-200">&#128218; Favorite Books</span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="mt-2 pr-12">
					<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
						{#each books as book}
							<Favorite col_1={book.col_1} col_2={book.col_2} />
						{/each}
					</ol>
				</dd>
			</Accordion.Content>
		</Accordion.Item>

		<!-- Podcasts -->
		<Accordion.Item value="podcasts">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-300">🎙️ Favorite Podcasts</span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="mt-2 pr-12">
					<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
						{#each podcasts as podcast}
							<Favorite col_1={podcast.col_1} col_2={podcast.col_2} />
						{/each}
					</ol>
				</dd>
			</Accordion.Content>
		</Accordion.Item>

		<!-- Movies -->
		<Accordion.Item value="movies">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-400">&#127871; Favorite Movies</span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="mt-2 pr-12">
					<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
						{#each movies as movie}
							<Favorite col_1={movie.col_1} />
						{/each}
					</ol>
				</dd>
			</Accordion.Content>
		</Accordion.Item>

		<!--TV Shows -->
		<Accordion.Item value="shows">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-500"> &#127916; Favorite TV Shows</span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="mt-2 pr-12">
					<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
						{#each books as book}
							<Favorite col_1={book.col_1} col_2={book.col_2} />
						{/each}
					</ol>
				</dd>
			</Accordion.Content>
		</Accordion.Item>

		<!--Favorite Places on Earth -->
		<Accordion.Item value="places">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-600">&#127758; Favorite Places on Earth</span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="mt-2 pr-12">
					<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
						{#each places as place}
							<Favorite col_1={place.col_1} col_2={place.col_2} />
						{/each}
					</ol>
				</dd>
			</Accordion.Content>
		</Accordion.Item>

		<!-- GOAT -->
		<Accordion.Item value="goat">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-700"> &#127936; Greatest of All Time </span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="mt-2 pr-12">
					<p class="font-bold text-gray-200 text-xl ml-4">Jordan.</p>
				</dd>
			</Accordion.Content>
		</Accordion.Item>
	</Accordion.Root>
</div>
