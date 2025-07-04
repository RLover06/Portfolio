<script lang="ts">
	import * as Accordion from '$lib/components/ui/accordion';
	import Favorite from '$lib/components/Favorite.svelte';

	const books = [
		{ icon1: '📖', col_1: 'The Little Prince', icon2: '✍️', col_2: 'Antoine de Saint-Exupéry' },
		{ icon1: '📖', col_1: '12 Rules for Life', icon2: '✍️', col_2: 'Jordan B. Peterson' },
		{ icon1: '📖', col_1: 'Hard Thing About Hard Things', icon2: '✍️', col_2: 'Ben Horowitz' },
		{ icon1: '📖', col_1: 'Zero to One', icon2: '✍️', col_2: 'Peter Thiel' },
		{ icon1: '📖', col_1: 'Rework', icon2: '✍️', col_2: 'Jason Fried • David Heinemeier Hanson' },
		{ icon1: '📖', col_1: 'Delivering Happiness', icon2: '✍️', col_2: 'Tony Hsieh' },
		{
			icon1: '📖',
			col_1: 'The Launch Pad: Inside Y Combinator',
			icon2: '✍️',
			col_2: 'Randal Stross',
		},
		{ icon1: '📖', col_1: 'Remote', icon2: '✍️', col_2: 'Jason Fried • David Heinemeier Hanson' },
		{ icon1: '📖', col_1: 'Shoe Dog', icon2: '✍️', col_2: 'Phil Knight' },
		{ icon1: '📖', col_1: 'Crazy Love', icon2: '✍️', col_2: 'Francis Chan' },
		{
			icon1: '📖',
			col_1: 'Tocqueville and the American Experiment',
			icon2: '✍️',
			col_2: 'William R. Cook',
		},
		{ icon1: '📖', col_1: 'Extreme Ownership', icon2: '✍️', col_2: 'Jocko Wilink • Leif Babin' },
		{ icon1: '📖', col_1: 'Outliers', icon2: '✍️', col_2: 'Malcom Gladwell' },
		{ icon1: '📖', col_1: 'David and Goliath', icon2: '✍️', col_2: 'Malcom Gladwell' },
		{
			icon1: '📖',
			col_1: 'A New Grammar Reference of Modern Spanish',
			icon2: '✍️',
			col_2: 'John Butt • Carmen Benjamin',
		},
	];

	const movies = [
		{ icon1: '🎥', col_1: "You've Got Mail" },
		{ icon1: '🎥', col_1: 'Interstellar' },
		{ icon1: '🎥', col_1: 'Blood Diamond' },
		{ icon1: '🎥', col_1: 'Angels in the Outfield' },
		{ icon1: '🎥', col_1: 'Lord of the Rings (Trilogy)' },
		{ icon1: '🎥', col_1: 'Gangs of New York' },
		{ icon1: '🎥', col_1: '100 Foot Journey' },
		{ icon1: '🎥', col_1: 'The Matrix' },
		{ icon1: '🎥', col_1: 'Training Day' },
		{ icon1: '🎥', col_1: 'Catch Me If You Can' },
	];

	const shows = [
		{ icon1: '📺', col_1: 'Severance' },
		{ icon1: '📺', col_1: 'Suits' },
		{ icon1: '📺', col_1: "That 70's Show" },
		{ icon1: '📺', col_1: 'Body Guard' },
		{ icon1: '📺', col_1: 'Line of Duty' },
		{ icon1: '📺', col_1: 'Dexter' },
		{ icon1: '📺', col_1: 'Cheers' },
		{ icon1: '📺', col_1: 'Yu Yu Hakusho' },
		{ icon1: '📺', col_1: 'True Detective' },
		{ icon1: '📺', col_1: 'Fargo' },
	];

	const places = [
		{
			icon1: '📍',
			col_1: 'The Woodlands, Texas',
			icon2: '⭐️',
			col_2: "I'm a hometown kind of guy",
		},
		{
			icon1: '📍',
			col_1: 'Tenerife, Spain',
			icon2: '⭐️',
			col_2: 'Incredible amount of microclimates',
		},
		{
			icon1: '📍',
			col_1: 'Medellín, Colombia',
			icon2: '⭐️',
			col_2: 'Lived here for 6 years',
		},
		{
			icon1: '📍',
			col_1: 'Santa Fé de Antioquia, Colombia',
			icon2: '⭐️',
			col_2: 'Perfectly slow pace of life',
		},
		{
			icon1: '📍',
			col_1: 'Denver, Colorado',
			icon2: '⭐️',
			col_2: 'Lived here for a year, Rocky Mountain Air',
		},
		{ icon1: '📍', col_1: 'Papagayo, Costa Rica', icon2: '⭐️', col_2: 'Great family memories' },
		{
			icon1: '📍',
			col_1: 'Rome, Italy',
			icon2: '⭐️',
			col_2: 'If Rome can fall, nothing is forever',
		},
		{ icon1: '📍', col_1: 'Maui, Hawaii', icon2: '⭐️', col_2: 'Never been more relaxed' },
		{ icon1: '📍', col_1: 'Nassau, Bahamas', icon2: '⭐️', col_2: 'More fond family memories' },
		{ icon1: '📍', col_1: 'Cusco, Peru', icon2: '⭐️', col_2: 'Ancient' },
		{ icon1: '📍', col_1: 'Lima, Peru', icon2: '⭐️', col_2: 'Ceviche' },
		{
			icon1: '📍',
			col_1: 'Florence, Italy',
			icon2: '⭐️',
			col_2: 'Refreshing taste of craftsmanship',
		},
		{
			icon1: '📍',
			col_1: 'San Pedro de Atacama, Chile',
			icon2: '⭐️',
			col_2: 'Surreal landscapes',
		},
		{ icon1: '📍', col_1: 'Kauai, Hawaii', icon2: '⭐️', col_2: 'Classic family memories' },
		{
			icon1: '📍',
			col_1: 'Grand Cayman, Cayman Islands',
			icon2: '⭐️',
			col_2: 'Islands are easy to love, stringrays!',
		},
		{ icon1: '📍', col_1: 'Lübbecke, Germany', icon2: '⭐️', col_2: 'First taste of Europe' },
		{
			icon1: '📍',
			col_1: 'Jardín, Colombia',
			icon2: '⭐️',
			col_2: "Named 'Garden' in Spanish for its beauty",
		},
		{ icon1: '📍', col_1: 'Madrid, Spain', icon2: '⭐️', col_2: 'All around underrated' },
		{ icon1: '📍', col_1: 'Granada, Spain', icon2: '⭐️', col_2: 'Creativity that inspires' },
		{ icon1: '📍', col_1: 'Paracas, Perú', icon2: '⭐️', col_2: 'Animals all over the place' },
		{
			icon1: '📍',
			col_1: 'Valle de Corcoa, Colombia',
			icon2: '⭐️',
			col_2: 'Tallest palm trees in the world',
		},
		{
			icon1: '📍',
			col_1: 'Villa de Leyva, Colombia',
			icon2: '⭐️',
			col_2: 'Great mix of relaxation + things to do',
		},
		{
			icon1: '📍',
			col_1: 'Santa Marta, Colombia',
			icon2: '⭐️',
			col_2: 'Major fan of Parque Tayrona',
		},
		{
			icon1: '📍',
			col_1: 'El Retiro, Colombia',
			icon2: '⭐️',
			col_2: 'Classic mountain town of Antioquia',
		},
		{
			icon1: '📍',
			col_1: 'Cartagena, Colombia',
			icon2: '⭐️',
			col_2: 'Historic Caribbean city',
		},
	];
</script>

<div class="mx-auto w-11/12 text-white md:w-3/5" id="favorites">
	<h2
		class="glow-green space-grotesk text-center text-3xl font-extrabold leading-9 text-green-400 sm:text-4xl sm:leading-10"
	>
		Favorites
	</h2>
	<Accordion.Root>
		<!-- Books -->
		<Accordion.Item value="books">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-300">&#128218; Favorite Books</span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="p-2">
					<ol class="ml-6 list-decimal text-base leading-6 text-gray-400">
						{#each books as book}
							<Favorite
								icon1={book.icon1}
								col_1={book.col_1}
								icon2={book.icon2}
								col_2={book.col_2}
							/>
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
				<dd class="p-2">
					<ol class="ml-6 list-decimal text-base leading-6 text-gray-400">
						{#each movies as movie}
							<Favorite icon1={movie.icon1} col_1={movie.col_1} />
						{/each}
					</ol>
				</dd>
			</Accordion.Content>
		</Accordion.Item>

		<!-- TV Shows -->
		<Accordion.Item value="shows">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-500"> &#127916; Favorite TV Shows</span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="p-2">
					<ol class="ml-6 list-decimal text-base leading-6 text-gray-400">
						{#each shows as show}
							<Favorite icon1={show.icon1} col_1={show.col_1} />
						{/each}
					</ol>
				</dd>
			</Accordion.Content>
		</Accordion.Item>

		<!-- Favorite Places on Earth -->
		<Accordion.Item value="places">
			<Accordion.Trigger class="hover:no-underline">
				<span class="text-lg font-medium text-green-600">&#127758; Favorite Places on Earth</span>
			</Accordion.Trigger>
			<Accordion.Content>
				<dd class="p-2">
					<ol class="ml-6 list-decimal text-base leading-6 text-gray-400">
						{#each places as place}
							<Favorite
								icon1={place.icon1}
								col_1={place.col_1}
								icon2={place.icon2}
								col_2={place.col_2}
							/>
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
					<p class="ml-4 text-xl font-bold text-gray-200">Jordan. 🏆 🏆 🏆 🏆 🏆 🏆</p>
				</dd>
			</Accordion.Content>
		</Accordion.Item>
	</Accordion.Root>
</div>
