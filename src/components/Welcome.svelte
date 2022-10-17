<script lang="ts">
	import IoIosClose from 'svelte-icons/io/IoIosClose.svelte';
	let welcomeVisible = true;
</script>

<div
	class={`w-full h-20 p-4 rounded-md bg-yellow-500 ${
		welcomeVisible ? 'flex' : 'hidden'
	} flex-row justify-between`}
>
	<h4 class="font-extralight text-[17px]">
		Welcome on Medium Blog built using Svelte Kit and Nest js
	</h4>
	<button class="h-8 w-8 text-black " on:click={() => (welcomeVisible = false)}>
		<IoIosClose />
	</button>
</div>
