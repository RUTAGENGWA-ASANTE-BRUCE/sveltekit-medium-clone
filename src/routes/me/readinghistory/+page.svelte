<script type="ts">
    	import Blog from '../../../components/Blog.svelte'
	import IoIosAdd from 'svelte-icons/io/IoIosAdd.svelte';
    	interface blog {
            title: string;
        profileName: string;
        profilePicture: string;
        type: string;
        description: string;
        views:number;
        image: string;
        createdAt: string;
        updatedAt: string;
	}

	let blogs: blog[] = [
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
			createdAt: '3 days ago',
            updatedAt: '3 days ago'
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
			createdAt: '3 days ago',
            updatedAt: '3 days ago'
		},
	];

</script>
<div class="space-y-12 py-6 ">
	<div class=" w-full p-5 bg-gray-100 flex flex-row justify-between">
        <p>You can clear your reading history for a fresh start.</p>
        <button class="w-fit px-3 bg-red-700 hover:bg-red-500 rounded-full text-sm py-2 text-white font-semibold">Clear history</button>
    </div>
    <div class="mt-5 space-y-4">
        {#each blogs as item}
        <Blog item={item} inHistory />
        {/each}
    </div>
</div>
