<script lang="ts">
    export let specialFrontComponent;
    interface link{
        title:string;
        path:string;
    }
    export let links:link[];
    export let selected:string;
   
</script>



<div class="w-full mt-8 border-b h-[49px] relative mt-">
    <div class="absolute top-1 flex-row flex space-x-4 ">
        <slot name="specialFrontComponent" />
        {#each links as link}
		<a href={`${link.path}`} class={`border-b pb-5 w-fit ${selected===link.title && 'border-black'}`}>{link.title}</a>
        {/each}
	</div>
</div>