<script type="ts">
    import TabNavigation from "../../../components/TabNavigation.svelte";
    let links=[
        {
            title:'Following',
            path:'/me/following'
        },
        {
            title:'Reading history',
            path:'/me/readinghistory'
        },
        {
            title:'Muted',
            path:'/me/settings/mute'
        },
        {
            title:'Suggestions',
            path:'/me/following/suggestions'
        },
    ]
</script>
<h1 class="text-[50px] font-bold">Refine recommendations</h1>
<p class="text-gray-500 my-5 ">Adjust recommendations by updating what you’re following, your reading history, and who you’ve muted.</p>
<TabNavigation links={links} />
<slot></slot>