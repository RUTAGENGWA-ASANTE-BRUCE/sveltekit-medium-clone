<script type="ts">
    import TabNavigation from "../../../components/TabNavigation.svelte";
    let links=[
        {
            title:'Drafts',
            path:'/me/stories/drafts'
        },
        {
            title:'Published',
            path:'/me/stories/public'
        },
        {
            title:'Responses',
            path:'/me/stories/responses'
        },
    ]
</script>
<div class="flex flex-low justify-between">

    <h1 class="text-[50px] font-bold">Your stories</h1>
    <div class="flex flex-row space-x-2 mt-6">
        <button class="px-3 rounded-full text-white font-semibold py-2 h-fit w-fit text-sm bg-[#1a8917]">Write a story </button>
        <button class="px-3 rounded-full text-black border-black h-fit w-fit border font-semibold py-2 text-sm">Import a story</button>
    </div>
</div>
<TabNavigation links={links} />
<slot></slot>