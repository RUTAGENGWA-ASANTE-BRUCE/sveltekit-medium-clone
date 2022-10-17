<script type="ts">
	import Draft from "../../../../components/Draft.svelte";

	interface draft {
		title: string;
		profileName: string;
		profilePicture: string;
		type: string;
		description: string;
		views: number;
		image: string;
		createdAt: string;
		updatedAt: string;
	}
	let drafts: draft[] = [
		{
			profileName: 'Jordan Poole',
			profilePicture:
				'https://phantom-marca.unidadeditorial.es/7f5738d024287b3132c34ba23ed503b5/resize/1320/f/jpg/assets/multimedia/imagenes/2022/10/08/16652073469932.jpg',
			title: 'Fight Between Jordan Poole and Draymond Green',
			description: "Warriors' Draymond Green Apologizes for Punching Jordan Poole",
			type: 'News',
			views: 3,
			image:
				'https://cloudfront-us-east-1.images.arcpublishing.com/advancelocal/63UKXXVFKRAQLBUDM3K4LKRXPQ.JPG',
			updatedAt: '3 days ago',
			createdAt: '3 days ago'
		},
		{
			profileName: 'Jordan Poole',
			profilePicture:
				'https://phantom-marca.unidadeditorial.es/7f5738d024287b3132c34ba23ed503b5/resize/1320/f/jpg/assets/multimedia/imagenes/2022/10/08/16652073469932.jpg',
			title: 'Fight Between Jordan Poole and Draymond Green',
			description: "Warriors' Draymond Green Apologizes for Punching Jordan Poole",
			type: 'News',
			views: 3,
			image:
				'https://cloudfront-us-east-1.images.arcpublishing.com/advancelocal/63UKXXVFKRAQLBUDM3K4LKRXPQ.JPG',
			updatedAt: '3 days ago',
			createdAt: '3 days ago'
		}
	];
</script>

<div class="space-y-12 py-6 ">
	{#if drafts.length > 0}
		{#each drafts as item}
			<Draft item={item}/>
		{/each}
	{:else}
		<p class="text-gray-500 mt-10 text-center">You have no saved drafts.</p>
	{/if}
</div>
