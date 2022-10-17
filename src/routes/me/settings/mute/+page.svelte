<script type="ts">
    let muteds=[];
    import NoDataYet from '../../../../components/NoDataYet.svelte';
	
</script>


<div class="space-y-12 py-6 ">
	
	
	{#if muteds.length > 0}
		<h1>Topics</h1>
	{:else}
		<NoDataYet title={''} suggestionsLink={'/'} />
	{/if}
</div>
