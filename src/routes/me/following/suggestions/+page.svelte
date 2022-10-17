<script type="ts">
	import TopicSuggestion from '../../../../components/TopicSuggestion.svelte';
	import FollowSuggestionSuggestion from './../../../../components/FollowSuggestion.svelte';
	interface followSuggestion {
		profilePicture: string;
		profileName: string;
		description: string;
	}
	let followSuggestions: followSuggestion[] = [
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
    interface topicSuggestion{
        title: string;
        stories: number;
        writers: number;
    }
    let topicSuggestions:topicSuggestion[]=[
        {
            title:"Technology",
            stories:200000,
            writers:130
        },
        {
            title:"Money",
            stories:2000,
            writers:5000
        },
        {
            title:"Business",
            stories:20311130,
            writers:8960000
        },
        
    ]


</script>

<div class="space-y-12 py-6 ">
	<div class="  space-y-4 flex flex-col pb-7 border-b">
		<h4 class="font-semibold text-[18px]">Who to follow</h4>
		<div class="flex flex-col space-y-6 flex-wrap">
			{#each followSuggestions as item}
				<FollowSuggestionSuggestion {item} />
			{/each}
		</div>
		<p class=" text-[#1a8917]">See more suggestions</p>
	</div>
    <div class="  space-y-4 flex flex-col pb-7 border-b">
		<h4 class="font-semibold text-[18px]">Topics to follow</h4>
		<div class="flex flex-col space-y-6 flex-wrap">
			{#each topicSuggestions as item}
				<TopicSuggestion {item} />
			{/each}
		</div>
		<p class=" text-[#1a8917]">See more suggestions</p>
	</div>
</div>
