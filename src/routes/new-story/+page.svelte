<script type="ts">
	/** @type {import('./$types').ActionData} */
	export let form;
	let files;
	import { flip } from 'svelte/animate';
	let imageToPost: string="";
	export let item;
	let title = '';
	let description = '';
	import MdMoreHoriz from 'svelte-icons/md/MdMoreHoriz.svelte';
	let titleInputVisible: boolean = true;
	let descriptionInputVisible: boolean = false;
	import MdAdd from 'svelte-icons/md/MdAdd.svelte';
	import { fly } from 'svelte/transition';
	let optionsVisible = false;
	import TiCameraOutline from 'svelte-icons/ti/TiCameraOutline.svelte';
	import MdShortText from 'svelte-icons/md/MdShortText.svelte';
	$: if (files) {
		// Note that `files` is of type `FileList`, not an Array:
		// https://developer.mozilla.org/en-US/docs/Web/API/FileList
		console.log(files);
		const reader = new FileReader();
		for (const file of files) {
			reader.readAsDataURL(file);
			reader.onload = (readerEvent) => {
				let imageUrl = readerEvent.target.result;
				if (imageUrl) {
					imageToPost = <string>imageUrl;
				}
			};
			optionsVisible=false;
			console.log(`${file.name}: ${file.size} bytes`);
			console.log('=============', imageToPost);
		}
	}
</script>

<div class="mt-5 space-y-7">
	<div class="flex flex-row  justify-between">
		<div class="flex flex-row space-x-2">
			<img
				src="https://cdn-icons-png.flaticon.com/512/5968/5968885.png"
				alt="Medium icon"
				class="w-10 h-10 object-fit"
			/>
			<p class="mt-2">Draft</p>
		</div>
		<div class="flex flex-row space-x-2">
			{#if title === '' && description === '' && imageToPost === ''}
				<button
					class="px-3 rounded-full text-white font-semibold py-1 h-fit w-fit text-sm bg-[#1a8917] opacity-50"
					disabled>Publish</button
				>
			{:else}
				<button
					class="px-3 rounded-full text-white font-semibold py-1 h-fit w-fit text-sm bg-[#1a8917]"
					>Publish</button
				>
			{/if}
			<button class="h-5 w-5 text-black mt-1">
				<MdMoreHoriz />
			</button>
		</div>
	</div>
	<div class="flex flex-row p-5 ">
		<div class="flex flex-row  w-12 relative">
			<button
				on:click={() => (optionsVisible = !optionsVisible)}
				class=" h-9 w-9 absolute bottom-5  rounded-full border border-black"
			>
				<MdAdd />
			</button>

			{#if optionsVisible}
				<div
					class="p-5 top-1 w-32 left-10 flex-row space-x-3  bg-white flex-1 bottom-5  absolute flex flex-nowrap"
					transition:fly={{ x: 20, duration: 500 }}
				>
					<div class={`h-8 w-8 rounded-full border border-black p-1.5 relative ${
						imageToPost!=="" ? 'text-red-500 border-red-500' : 'border black text-black'
					}`}>
						<input
							type="file"
							class="max-h-[25px] -left-[0px] bottom-1 cursor-pointer opacity-0 max-w-[28px] absolute"
							name="file"
							bind:files
							accept="image/*"
						/>
						<TiCameraOutline />
					</div>
					<button
						on:click={() => {
							descriptionInputVisible = !descriptionInputVisible;
							optionsVisible = false;
						}}
						class={`h-8 w-8 rounded-full border border-black p-1.5 ${
							descriptionInputVisible ? 'text-red-500 border-red-500' : 'border black text-black'
						}`}
					>
						<MdShortText />
					</button>
				</div>
			{/if}
		</div>

		<form class="px-5 flex-1">
			{#if titleInputVisible}
				<textarea
					rows={title.length / 10 > 0 ? Math.round(title.length / 19 + 0.5) : 1}
					class=" scrollbar-hide text-[20px] sm:text-[30px] md:text-[40px] lg:text-[50px] h-fit placeholder-zinc-400 font-serif outline-none border-none"
					placeholder="Title"
					autofocus
					name="title"
					bind:value={title}
				/>
			{/if}
			{#if descriptionInputVisible}
				<textarea
				rows={description.length / 10 > 0 ? Math.round(description.length / 19 + 0.5) : 1}

					class="scrollbar-hide o text-[20px] sm:text-[30px] md:text-[40px] lg:text-[50px] h-fit placeholder-zinc-400 font-serif outline-none border-none"
					placeholder="Tell your story"
					name="description"
					bind:value={description}
				/>
			{/if}
			{#if imageToPost !== ''}
				<img alt="" src={imageToPost} class="h-96 w-full object-cover" />
			{/if}
		</form>
	</div>
</div>

<style>
	.scrollbar-hide::-webkit-scrollbar {
		display: none;
	}
</style>
