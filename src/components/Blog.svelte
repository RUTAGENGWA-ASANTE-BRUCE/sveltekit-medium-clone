<script>
	import TiBookmark from 'svelte-icons/ti/TiBookmark.svelte';
	import FaMinusCircle from 'svelte-icons/fa/FaMinusCircle.svelte';
	import IoIosMore from 'svelte-icons/io/IoIosMore.svelte';
	export let item;
</script>

<div class="w-full pb-10 border-b">
	<div class="flex flex-row space-x-1.5">
		<img class="rounded-full h-6 w-6" src={item.profilePicture} alt={item.profileName} />
		<p class="font-semibold text-[13px]">
			{item.profileName} . <span class="text-gray-500">{item.addedAt}</span>
		</p>
	</div>
	<div class="flex flex-row justify-between">
		<div class="w-4/6 flex flex-col space-y-2">
			<h5 class="text-xl font-bold">{item.title}</h5>
			<p class="">{item.description}</p>
			<div class=" flex flex-row justify-between">
				<div class="flex mt-[75px] flex-row space-x-1 text-sm">
					<p class=" p-1 pl-1.5 min-w-[50px] bg-gray-200 rounded-full">
						{item.type}
					</p>
					<p class="text-gray-500 mt-1">
						. {item.views > 5 ? 'Popular on Medium' : 'Selected for you'}
					</p>
				</div>
				<div class="flex mt-[75px] flex-row space-x-3 text-gray-500">
					<div class="h-6 w-6  ">
						<TiBookmark />
					</div>
					<div class="h-6 w-6  ">
						<FaMinusCircle />
					</div>
					<div class="h-6 w-6 text-black  ">
						<IoIosMore />
					</div>
				</div>
			</div>
		</div>
		<img class="h-40 w-40 object-fit" src={item.image} alt={item.image} />
	</div>
</div>
