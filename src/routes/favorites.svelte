<script lang="ts">
	import * as Accordion from '$lib/components/ui/accordion';
	import Favorite from '$lib/components/favorite.svelte';

	const favorites = {
		books: false,
		movies: false,
		shows: false,
		places: false,
		goat: false
	};

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
		{ col_1: 'Medellín, Colombia', col_2: 'Lived here for 5 years, más paisa que una arepa' },
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

<div class="w-2/3 mx-auto text-white">
	<h2 class="text-center text-3xl leading-9 font-extrabold text-green-400 sm:text-4xl sm:leading-10 glow-green">Favorites</h2>
	<Accordion.Root>
		<Accordion.Item value="item-1">
			<Accordion.Trigger>Favorite Books</Accordion.Trigger>
			<Accordion.Content>
				{#each books as book}
					<Favorite col_1={book.col_1} col_2={book.col_2} />
				{/each}
			</Accordion.Content>
		</Accordion.Item>
	</Accordion.Root>
</div>

<!-- Favorites -->
<div id="favorites" class="bg-slate-950">
	<div class="max-w-screen-xl mx-auto py-12 px-4 sm:py-16 sm:px-6 lg:px-8">
		<div class="max-w-3xl mx-auto">
			<h2 class="text-center text-3xl leading-9 font-extrabold text-green-400 sm:text-4xl sm:leading-10 glow-green">Favorites</h2>
			<div class="mt-6 border-t-2 border-gray-200 pt-6">
				<dl>
					<!-- Books -->
					<div>
						<dt class="text-lg leading-7">
							<button on:click={() => (favorites.books = !favorites.books)} class="text-left w-full flex justify-between items-start text-gray-400 focus:outline-none focus:text-gray-900">
								<span class="font-medium text-green-300">&#128218; Favorite Books</span>
								<span class="ml-6 h-7 flex items-center">
									<svg class="h-6 w-6 transform" stroke="currentColor" fill="none" viewBox="0 0 24 24">
										<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
									</svg>
								</span>
							</button>
						</dt>
						{#if favorites.books}
							<dd class="mt-2 pr-12">
								<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
									{#each books as book}
										<Favorite col_1={book.col_1} col_2={book.col_2} />
									{/each}
								</ol>
							</dd>
						{/if}
					</div>

					<!-- Movies -->
					<div class="mt-6 border-t border-gray-200 pt-6">
						<div>
							<dt class="text-lg leading-7">
								<button on:click={() => (favorites.movies = !favorites.movies)} class="text-left w-full flex justify-between items-start text-gray-400 focus:outline-none focus:text-gray-900">
									<span class="font-medium text-green-400">&#127871; Favorite Movies</span>
									<span class="ml-6 h-7 flex items-center">
										<svg class="h-6 w-6 transform" stroke="currentColor" fill="none" viewBox="0 0 24 24">
											<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
										</svg>
									</span>
								</button>
							</dt>
							{#if favorites.movies}
								<dd class="mt-2 pr-12">
									<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
										{#each movies as movie}
											<Favorite col_1={movie.col_1} />
										{/each}
									</ol>
								</dd>
							{/if}
						</div>
					</div>

					<!-- Shows -->
					<div class="mt-6 border-t border-gray-200 pt-6">
						<div>
							<dt class="text-lg leading-7">
								<button on:click={() => (favorites.shows = !favorites.shows)} class="text-left w-full flex justify-between items-start text-gray-400 focus:outline-none focus:text-gray-900">
									<span class="font-medium text-green-500"> &#127916; Favorite TV Shows</span>
									<span class="ml-6 h-7 flex items-center">
										<svg class="h-6 w-6 transform" stroke="currentColor" fill="none" viewBox="0 0 24 24">
											<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
										</svg>
									</span>
								</button>
							</dt>
							{#if favorites.shows}
								<dd class="mt-2 pr-12">
									<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
										{#each shows as show}
											<Favorite col_1={show.col_1} />
										{/each}
									</ol>
								</dd>
							{/if}
						</div>
					</div>

					<!-- Places -->
					<div class="mt-6 border-t border-gray-200 pt-6">
						<div>
							<dt class="text-lg leading-7">
								<button on:click={() => (favorites.places = !favorites.places)} class="text-left w-full flex justify-between items-start text-gray-400 focus:outline-none focus:text-gray-900">
									<span class="font-medium text-green-600">&#127758; Favorite Places on Earth</span>
									<span class="ml-6 h-7 flex items-center">
										<svg class="h-6 w-6 transform" stroke="currentColor" fill="none" viewBox="0 0 24 24">
											<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
										</svg>
									</span>
								</button>
							</dt>
							{#if favorites.places}
								<dd class="mt-2 pr-12">
									<ol class="list-decimal text-base leading-6 text-gray-400 ml-6">
										{#each places as place}
											<Favorite col_1={place.col_1} col_2={place.col_2} />
										{/each}
									</ol>
								</dd>
							{/if}
						</div>
					</div>

					<!-- GOAT -->
					<div class="mt-6 border-t border-gray-200 pt-6">
						<div>
							<dt class="text-lg leading-7">
								<button on:click={() => (favorites.goat = !favorites.goat)} class="text-left w-full flex justify-between items-start text-gray-400 focus:outline-none focus:text-gray-900">
									<span class="font-medium text-green-700"> &#127936; Greatest of All Time </span>
									<span class="ml-6 h-7 flex items-center">
										<svg class="h-6 w-6 transform" stroke="currentColor" fill="none" viewBox="0 0 24 24">
											<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
										</svg>
									</span>
								</button>
							</dt>
							{#if favorites.goat}
								<dd class="mt-2 pr-12">
									<p class="font-bold text-gray-200 text-xl ml-4">Jordan.</p>
								</dd>
							{/if}
						</div>
					</div>
				</dl>
			</div>
		</div>
	</div>
</div>
