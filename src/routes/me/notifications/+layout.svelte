<script type="ts">
	import TabNavigation from '../../../components/TabNavigation.svelte';
	interface link {
		title: string;
		path: string;
	}
	let links: link[] = [
		{
			title: 'All',
			path: '/'
		},
		{
			title: 'Responses',
			path: '/followingFeed'
		}
	];
</script>

<h1 class="text-[50px] font-bold">Notifications</h1>
<TabNavigation {links} selected={'All'} />
<slot></slot>