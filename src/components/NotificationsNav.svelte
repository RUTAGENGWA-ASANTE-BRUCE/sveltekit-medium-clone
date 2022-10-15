<script lang="ts">
	import IoIosAdd from 'svelte-icons/io/IoIosAdd.svelte';
    export let selected:string;
    import IoIosClose from 'svelte-icons/io/IoIosClose.svelte';
    let welcomeVisible=true;
</script>



<div class="w-full mt-8 border-b h-[49px] relative mt-">
	<div class="absolute top-1 flex-row flex space-x-4 ">
		<a href={'/'} class={`border-b pb-5 w-fit ${selected==='All' && 'border-black'}`}>All</a>
		<a href={'/followingFeed'} class={`border-b pb-5  w-fit ${selected==='Responses' && 'border-black'}`}>Responses</a>
	</div>
</div>