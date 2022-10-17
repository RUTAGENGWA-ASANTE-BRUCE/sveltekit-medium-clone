<script type="ts">
	import NoDataYet from '../../../components/NoDataYet.svelte';
	import FollowSuggestionSuggestion from './../../../components/FollowSuggestion.svelte';
	let publications = [];
	let topics = [];
	interface followSuggestion {
		profilePicture: string;
		profileName: string;
		description: string;
	}
	let follows: followSuggestion[] = [
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

<div class="space-y-12 py-6 ">
	{#if follows.length > 0}
		<div class="  space-y-4 flex flex-col pb-7 border-b">
			<h4 class="font-semibold text-[18px]">{follows.length} Writers</h4>
			<div class="flex flex-col space-y-6 flex-wrap">
				{#each follows as item}
					<FollowSuggestionSuggestion {item} followed />
				{/each}
			</div>
			<p class=" text-[#1a8917]">See more suggestions</p>
		</div>
	{:else}
		<NoDataYet title={'Writers'} suggestionsLink={'/'} />
	{/if}
	{#if publications.length > 0}
		<h1>Publications</h1>
	{:else}
		<NoDataYet title={'Publications'} suggestionsLink={'/'} />
	{/if}
	{#if topics.length > 0}
		<h1>Topics</h1>
	{:else}
		<NoDataYet title={'Topics'} suggestionsLink={'/'} />
	{/if}
</div>
