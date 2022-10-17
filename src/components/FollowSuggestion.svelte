<script type="ts">
    interface item{
        profileName: string;
        profilePicture: string;
        description: string;
    }
	export let item:item;
	export let followed:boolean;
    export let locatedInWidgets:boolean; 
</script>

<div class="w-full flex flex-row space-x-2">
	<img class="rounded-full h-12 w-12" src={item.profilePicture} alt={item.profileName} />
	<div class="flex-1 flex flex-row justify-between w-full flex-wrap">
		<div class="flex flex-col w-full sm:w-[75%] space-y-1">
			<h4 class="font-bold text-[17px]">{item.profileName}</h4>
			<p class="text-gray-500 text-xs">
				{item.description.slice(0, 69)}...
			</p>
		</div>
		<button
			class={`${locatedInWidgets?'border-black text-black':(followed?"border-[#1a8917] text-[#1a8917] ":" bg-[#1a8917] border-[#1a8917] hover text-white font-semibold")} mt-5 h-fit  flex  space-x-2 flex-row rounded-full text-xs border px-4 py-2 w-fit`}
			>{followed?'Following':"Follow"}</button
		>
	</div>
</div>
