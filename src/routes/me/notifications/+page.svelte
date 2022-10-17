<script type="ts">
	let notifications = [];
</script>

<div class="space-y-12 py-6 ">
	{#if notifications.length > 0}
	<div />
	{:else}
	<p class="text-gray-500">You're all caught up.</p>
	{/if}
</div>
