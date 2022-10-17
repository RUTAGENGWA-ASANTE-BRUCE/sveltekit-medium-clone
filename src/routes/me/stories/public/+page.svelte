<script type="ts">
	let publicStroies = [];
</script>

<div class="space-y-12 py-6 ">
	{#if publicStroies.length > 0}
	<div />
	{:else}
	<p class="text-gray-500  text-center mt-10">You haven’t published any public stories yet.</p>
	{/if}
</div>
