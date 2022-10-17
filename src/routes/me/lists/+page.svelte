<script lang="ts">
	import IoIosClose from 'svelte-icons/io/IoIosClose.svelte';
	let createListGroup = true;
</script>

<div class="space-y-12 py-6 ">
	<div
		class={`w-full py-10 space-y-4 px-7 rounded-md bg-[#1a8917] ${
			createListGroup ? 'flex' : 'hidden'
		} flex-col`}
	>
		<div class="lex-row justify-between flex">
			<h4 class=" text-white font-bold  text-2xl w-fit md:w-3/6">
				Create a list to easily organize and share stories
			</h4>
			<button class="h-8 w-8 text-white " on:click={() => (createListGroup = false)}>
				<IoIosClose />
			</button>
		</div>
		<button class="px-3 rounded-full text-white font-semibold py-2 h-fit w-fit text-sm bg-black"
			>Start a list</button
		>
	</div>
    <div class="flex flex-row w-full  rounded-md border bg-gray-100">
        <div class="w-[55%] flex flex-col space-y-16 py-7 pl-7">
            <h4 class="  font-bold  text-2xl ">
				Reading list
			</h4>
            <button class="px-3 rounded-full text-black font-semibold py-2 h-fit w-fit text-sm border border-black"
			>View list</button
		>
        </div>
        <div class="w-[45%] flex flex-row">
            <div class="w-[55%] border-r-2 border-white bg-black h-full">
                <div class="h-full w-full rounded-full bg-gray-500"></div>
            </div>
            <div class="w-[25%] border-r-2 border-white bg-black h-full">
                <div class="h-full w-full rounded-r-full bg-gray-500"></div>
            </div>
            <div class="w-[20%]  border-white bg-black h-full">
                <div class="h-full w-full rounded-r-full bg-gray-500"></div>
            </div>
        </div>
    </div>
</div>
