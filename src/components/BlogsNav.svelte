<script lang="ts">
	import IoIosAdd from 'svelte-icons/io/IoIosAdd.svelte';
    export let selected:string;
    import IoIosClose from 'svelte-icons/io/IoIosClose.svelte';
    let welcomeVisible=true;
</script>

<div class={`w-full h-20 p-4 rounded-md bg-yellow-500 ${welcomeVisible?'flex':'hidden'} flex-row justify-between`}>
	<h4 class="font-extralight text-[17px]">
		Welcome on Medium Blog built using Svelte Kit and Nest js
	</h4>
	<button class="h-8 w-8 text-black " on:click={()=>welcomeVisible=false}>
		<IoIosClose />
	</button>
</div>

<div class="w-full mt-8 border-b h-[49px] relative mt-">
	<div class="absolute top-1 flex-row flex space-x-4 ">
		<div class="border-b w-fit  ">
			<div class="h-[26.5px] w-8 text-black  "    >
				<IoIosAdd />
			</div>
		</div>
		<a href={'/'} class={`border-b pb-5 w-fit ${selected==='For you' && 'border-black'}`}>For you</a>
		<a href={'/followingFeed'} class={`border-b pb-5  w-fit ${selected==='Following' && 'border-black'}`}>Following</a>
	</div>
</div>