<script lang="ts">
	import FollowSuggestion from './FollowSuggestion.svelte';
	import IoIosSearch from 'svelte-icons/io/IoIosSearch.svelte';
	import IoIosClose from 'svelte-icons/io/IoIosClose.svelte';
	import IoIosAdd from 'svelte-icons/io/IoIosAdd.svelte';
	import TiBookmark from 'svelte-icons/ti/TiBookmark.svelte';
	let topics = [
		'Technology',
		'Money',
		'Business',
		'productivity',
		'Psychology',
		'Mindfulness',
		'Art'
	];
	interface staffPick {
		profilePicture: string;
		profileName: string;
		description: string;
	}
	interface follow {
		profilePicture: string;
		profileName: string;
		description: string;
	}
	let staffPicks: staffPick[] = [
		{
			profilePicture:
				'https://phantom-marca.unidadeditorial.es/7f5738d024287b3132c34ba23ed503b5/resize/1320/f/jpg/assets/multimedia/imagenes/2022/10/08/16652073469932.jpg',
			profileName: 'Jordan Poole',
			description: 'Jordan Poole is the only winner after getting sucker punched by Draymond Green.'
		},
		{
			profilePicture:
				'https://phantom-marca.unidadeditorial.es/7f5738d024287b3132c34ba23ed503b5/resize/1320/f/jpg/assets/multimedia/imagenes/2022/10/08/16652073469932.jpg',
			profileName: 'Jordan Poole',
			description: 'Jordan Poole is the only winner after getting sucker punched by Draymond Green.'
		},
		{
			profilePicture:
				'https://phantom-marca.unidadeditorial.es/7f5738d024287b3132c34ba23ed503b5/resize/1320/f/jpg/assets/multimedia/imagenes/2022/10/08/16652073469932.jpg',
			profileName: 'Jordan Poole',
			description: 'Jordan Poole is the only winner after getting sucker punched by Draymond Green.'
		}
	];
	let follows: follow[] = [
		{
			profilePicture:
				'https://phantom-marca.unidadeditorial.es/7f5738d024287b3132c34ba23ed503b5/resize/1320/f/jpg/assets/multimedia/imagenes/2022/10/08/16652073469932.jpg',
			profileName: 'Jordan Poole',
			description: 'Jordan Poole is the only winner after getting sucker punched by Draymond Green.'
		},
		{
			profilePicture:
				'https://phantom-marca.unidadeditorial.es/7f5738d024287b3132c34ba23ed503b5/resize/1320/f/jpg/assets/multimedia/imagenes/2022/10/08/16652073469932.jpg',
			profileName: 'Jordan Poole',
			description: 'Jordan Poole is the only winner after getting sucker punched by Draymond Green.'
		},
		{
			profilePicture:
				'https://phantom-marca.unidadeditorial.es/7f5738d024287b3132c34ba23ed503b5/resize/1320/f/jpg/assets/multimedia/imagenes/2022/10/08/16652073469932.jpg',
			profileName: 'Jordan Poole',
			description: 'Jordan Poole is the only winner after getting sucker punched by Draymond Green.'
		}
	];
</script>

<div
	class="px-10 py-2 max-h-screen col-span-3 hidden lg:flex flex-col space-y-9  overflow-y-scroll scrollbar-hide  "
>
	<div
		class="mt-2 flex items-center space-x-2 flex-row rounded-full border border-black p-2  text-gray-400"
	>
		<div class="h-5 w-5 text-black ">
			<IoIosSearch />
		</div>
		<input type="text" placeholder="Search" class="bg-transparent outline-none flex-1" />
	</div>
	<div class="  space-y-4 flex flex-col">
		<div class="flex flex-row  space-x-1.5">
			<div class="h-2 w-2 rounded-full mt-2.5    bg-[#1a8917]" />

			<p class="font-semibold text-[18px]">Staff Picks</p>
		</div>

		<div class=" space-y-5">
			{#each staffPicks as item}
				<div>
					<a href={`/recipes/${item.profilePicture}`} class="flex flex-row space-x-1.5">
						<img class="rounded-full h-6 w-6" src={item.profilePicture} alt={item.profileName} />
						<p class="font-semibold text-[13px]">{item.profileName}</p>
					</a>
					<p class="font-bold text-[17px] mt-1">{item.description}</p>
				</div>
			{/each}
		</div>
		<p class=" text-sm text-[#1a8917]">See the full list</p>
	</div>
	<div class="mt-4 w-full space-y-10 flex flex-col bg-blue-200 rounded-md  p-5">
		<div class="flex flex-row justify-between">
			<h4 class="font-bold text-[17px]">Writting on Medium</h4>
			<div class="h-8 w-8 text-black ">
				<IoIosClose />
			</div>
		</div>
		<div class="space-y-1.5 font-semibold text-[15px]">
			<p>New Writer FAQ</p>
			<p>Expert writing advice</p>
			<p>Grow your readership</p>
		</div>
		<button class=" bg-black rounded-full w-fit px-3 py-2 text-white text-xs font-bold "
			>Start writing</button
		>
	</div>
	<div class=" items-center border-b pb-7 flex flex-col space-y-3">
		<div class="w-fit flex flex-row ">
			<img
				src="https://cdn-icons-png.flaticon.com/512/5968/5968885.png"
				alt="Medium icon"
				class="w-8 h-8 object-fit"
			/>
			<div class="h-8 w-8 text-black ">
				<IoIosAdd />
			</div>
			<img src="https://links.papareact.com/drq" alt="Medium icon" class="w-10 h-10 object-fit" />
		</div>
		<p class="w-5/6 text-center">Dicover Medium writers you already follow on Twitter.</p>
		<div class="flex flex-col items-center  w-full justify-center">
			<div class="mt-5  flex  space-x-2 flex-row rounded-full border border-black p-2 w-fit">
				<img src="https://links.papareact.com/drq" alt="Medium icon" class="w-8 h-8 object-fit" />
				<p class="">Connect to Twitter</p>
			</div>
			<p class="mt-5 underline text-gray-500">Maybe Later</p>
		</div>
	</div>
	<div class="  space-y-4 flex flex-col">
		<h4 class="font-semibold text-[18px]">Recommended topics</h4>
		<div class="flex flex-row gap-3 flex-wrap">
			{#each topics as item}
				<p class=" p-3 min-w-[50px] bg-gray-200 rounded-full">
					{item}
				</p>
			{/each}
		</div>
	</div>
	<div class="  space-y-4 flex flex-col">
		<h4 class="font-semibold text-[18px]">Who to follow</h4>
		<div class="flex flex-col gap-4 flex-wrap">
			{#each follows as item}
				<FollowSuggestion {item} locatedInWidgets />
			{/each}
		</div>
		<p class=" text-[#1a8917]">See more suggestions</p>
	</div>
	<div class="  space-y-4 flex flex-col">
		<h4 class="font-semibold text-[18px]">Developer description</h4>
		<div class="flex flex-row gap-3 flex-wrap">
			<p class="min-w-[50px] text-gray-500 ">
				This site was created by RUTAGENGWA Asante Bruce not for commercial purpose but for
				SvelteKit eductaion prupose
			</p>
		</div>
	</div>
</div>

<style>
	.scrollbar-hide::-webkit-scrollbar {
		display: none;
	}
</style>
