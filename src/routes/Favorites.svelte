<script lang="ts">
	import * as Accordion from '$lib/components/ui/accordion';
	import Favorite from '$lib/components/Favorite.svelte';

	const books = [
		{ icon1: '📖', col_1: 'The 48 Laws of Power', icon2: '✍️', col_2: 'The 48 Laws of Power' },
		{ icon1: '📖', col_1: 'Thus Spoke Zarathustra', icon2: '✍️', col_2: 'Friedrich Nietzsche' },
		{ icon1: '📖', col_1: 'The secrets of the millionaire mind', icon2: '✍️', col_2: 'T. Harv Eker' },
		{ icon1: '📖', col_1: 'Zero to One', icon2: '✍️', col_2: 'Peter Thiel' },
		{ icon1: '📖', col_1: 'Atomic Habits', icon2: '✍️', col_2: 'James Clear' },
		{ icon1: '📖', col_1: 'Delivering Happiness', icon2: '✍️', col_2: 'Tony Hsieh' },
		{
			icon1: '📖',
			col_1: 'The Launch Pad: Inside Y Combinator',
			icon2: '✍️',
			col_2: 'Randal Stross',
		},
		{ icon1: '📖', col_1: 'Remote', icon2: '✍️', col_2: 'Jason Fried • David Heinemeier Hanson' },
		{ icon1: '📖', col_1: 'Shoe Dog', icon2: '✍️', col_2: 'Phil Knight' },
		{ icon1: '📖', col_1: 'Rich Dad, Poor Dad', icon2: '✍️', col_2: 'Robert Kiyosaki y Sharon Lechter' },
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
		{ icon1: '🎥', col_1: "Oppenheimer" },
		{ icon1: '🎥', col_1: 'Interstellar' },
		{ icon1: '🎥', col_1: 'Einstein and Eddington' },
		{ icon1: '🎥', col_1: 'A Spacetime Odyssey' },
		{ icon1: '🎥', col_1: 'an exceptional gift' },
		{ icon1: '🎥', col_1: 'The measurement of the world' },
		{ icon1: '🎥', col_1: 'Social network' },
		{ icon1: '🎥', col_1: 'Radioactive' },
		{ icon1: '🎥', col_1: 'lucy' },
		{ icon1: '🎥', col_1: 'Unlimited' },
	];

	const shows = [
		{ icon1: '📺', col_1: 'The Big Bang Theory' },
		{ icon1: '📺', col_1: 'Two and a Half Men' },
		{ icon1: '📺', col_1: "That 70's Show" },
		{ icon1: '📺', col_1: 'Cosmos' },
		{ icon1: '📺', col_1: 'One Piece' },
		{ icon1: '📺', col_1: 'Dragon Ball' },
		{ icon1: '📺', col_1: 'Lucifer' },
		{ icon1: '📺', col_1: 'The Money Heist' },
		{ icon1: '📺', col_1: 'The Walking Dead' },
		{ icon1: '📺', col_1: 'Breaking Bad' },
	];

	const places = [
		{
			icon1: '📍',
			col_1: 'Buenavista, Cordoba',
			icon2: '⭐️',
			col_2: "I'm a hometown kind of guy",
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
			col_1: 'Florence, Italy',
			icon2: '⭐️',
			col_2: 'Refreshing taste of craftsmanship',
		},

		{
			icon1: '📍',
			col_1: 'Jardín, Colombia',
			icon2: '⭐️',
			col_2: "Named 'Garden' in Spanish for its beauty",
		},
		{
			icon1: '📍',
			col_1: 'Valle de Corcoa, Colombia',
			icon2: '⭐️',
			col_2: 'Tallest palm trees in the world',
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
