<script type="ts">
    export let title:string;
    export let suggestionsLink:string;
</script>

<div class="  space-y-4 flex flex-col pb-7 border-b">
    <h4 class="font-semibold text-[18px]">{title}</h4>
	<p class="text-gray-500 text-center w-full">You haven’t followed any publications yet.</p>
	<a href={suggestionsLink} class=" text-[#1a8917] text-center w-full">See more suggestions</a>
</div>