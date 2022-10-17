<script type="ts">
    interface item{
        title: string;
        stories: number;
        writers: number;
    }
    import FaBook from 'svelte-icons/fa/FaBook.svelte'
	export let item:item;
</script>

<div class="w-full flex flex-row space-x-2">
	<div class="bg-gray-200 h-12 w-12 rounded-full justify-center flex items-center">
        <div class="h-4 w-4 rotate-45 text-gray-600">
            <FaBook />
        </div>
    </div>
	<div class="flex-1 flex flex-row justify-between w-full flex-wrap">
		<div class="flex flex-col w-full sm:w-[75%] space-y-1">
			<h4 class="font-bold text-[17px]">{item.title}</h4>
			<p class="text-gray-500 text-xs">
				{item.stories.toString.length>4?`${item.stories.toString.slice(0,3)}K`: `${item.stories}`} Stories .  {item.writers.toString.length>4?`${item.writers.toString.slice(0,3)}K`: `${item.writers}`} Writers
			</p>
		</div>
		<button
			class={`bg-[#1a8917] border-[#1a8917] hover:bg-green-[700] text-white font-semibold" mt-5 h-fit  flex  space-x-2 flex-row rounded-full text-xs border px-4 py-2 w-fit`}
			>Follow</button
		>
	</div>
</div>
