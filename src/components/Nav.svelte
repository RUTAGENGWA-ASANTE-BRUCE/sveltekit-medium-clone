<script lang="ts">
	import FaHome from 'svelte-icons/fa/FaHome.svelte';
	import IoIosNotificationsOutline from 'svelte-icons/io/IoIosNotificationsOutline.svelte';
	import IconButton from '@smui/icon-button';
	import MdBookmarkBorder from 'svelte-icons/md/MdBookmarkBorder.svelte';
	import IoIosPaper from 'svelte-icons/io/IoIosPaper.svelte';
	import FaEdit from 'svelte-icons/fa/FaEdit.svelte';
	var link = 0;
	const changeSelectedLink = (number: number) => {
		link = number;
		console.log(number);
	};
</script>

<div class="hidden md:flex items-center justify-center flex-col min-h-screen border-r md:w-20">
	<div class="flex flex-col gap-32">
		<img
			src="https://cdn-icons-png.flaticon.com/512/5968/5968885.png"
			alt="Medium icon"
			class="w-10 h-10 object-fit"
		/>
		<div class="flex flex-col gap-5">
			<a href={'/'}>
				<IconButton
					on:click={() => {
						link = 1;
					}}
					ripple={false}
				>
					<div
						class={`${
							link === 1 ? 'text-black' : 'text-gray-400'
						} w-10 h-10 active:bg-gray-200 hover:bg-gray-100 rounded-full p-2`}
					>
						<FaHome />
					</div>
				</IconButton>
			</a>
			<a href={'/notifications'}>
				<IconButton
					on:click={() => {
						link = 2;
					}}
					ripple={false}
				>
					<div
						class={`${
							link === 2 ? 'text-black' : 'text-gray-400'
						} w-10 h-10 active:bg-gray-200 hover:bg-gray-100 rounded-full p-2`}
					>
						<IoIosNotificationsOutline />
					</div>
				</IconButton>
			</a>
			<IconButton
				on:click={() => {
					link = 3;
				}}
				ripple={false}
			>
				<div
					class={`${
						link === 3 ? 'text-black' : 'text-gray-400'
					} w-10 h-10 active:bg-gray-200 hover:bg-gray-100 rounded-full p-2`}
				>
					<MdBookmarkBorder />
				</div>
			</IconButton>
			<IconButton
				on:click={() => {
					link = 4;
				}}
				ripple={false}
			>
				<div
					class={`${
						link === 4 ? 'text-black' : 'text-gray-400'
					} w-10 h-10 active:bg-gray-200 hover:bg-gray-100 rounded-full p-2`}
				>
					<IoIosPaper />
				</div>
			</IconButton>
			<hr class="bg-gray-200 w-12" />
			<IconButton
				on:click={() => {
					link = 5;
				}}
				ripple={false}
			>
				<div
					class={`${
						link === 5 ? 'text-black' : 'text-gray-400'
					} w-10 h-10 active:bg-gray-200 hover:bg-gray-100 rounded-full p-2`}
				>
					<FaEdit />
				</div>
			</IconButton>
		</div>
		<div class="flex items-center justify-center rounded-full h-10 w-10 bg-blue-500">
			<p class="text-white text-lg font-bold">B</p>
		</div>
	</div>
</div>
