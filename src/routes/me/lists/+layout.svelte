<script type="ts">
    import TabNavigation from "../../../components/TabNavigation.svelte";
    let links=[
        {
            title:'Saved',
            path:'/me/lists/'
        },
        {
            title:'Highlists',
            path:'/me/lists/highlights'
        },
    ]
</script>
<div class="flex flex-low justify-between">

    <h1 class="text-[50px] font-bold">Your lists</h1>
    <div class="flex flex-row space-x-2 mt-6">
        <button class="px-3 rounded-full text-white font-semibold py-2 h-fit w-fit text-sm bg-[#1a8917]">New list</button>
    </div>
</div>
<TabNavigation links={links} />
<slot></slot>