<script type="ts">
	let responses = [];
</script>

<div class="space-y-12 py-6 ">
	{#if responses.length > 0}
	<div />
	{:else}
	<p class="text-gray-500  text-center mt-10">You don't have story responses.</p>
	{/if}
</div>
