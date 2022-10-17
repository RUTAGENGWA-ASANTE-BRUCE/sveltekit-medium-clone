<script type="ts">
    interface item{
        title: string;
        profileName: string;
        profilePicture: string;
        type: string;
        description: string;
        views:number;
        image: string;
        createdAt: string;
        updatedAt: string;
    }
    export let item: item;
    import IoIosArrowDown from 'svelte-icons/io/IoIosArrowDown.svelte'
</script>

<div class="  space-y-4 flex flex-col pb-7 border-b">
    <h4 class="font-semibold text-[18px]">{item.title}</h4>
    <div class="flex flex-row space-x-3">

        <p class="text-gray-500 ">{item.updatedAt===item.createdAt?`Created ${item.createdAt}`:`Last edited  ${item.updatedAt}`} . {item.title.split(" ").length} words so far</p>  
         <button class="h-5 w-5 text-gray-500 mt-1">
            <IoIosArrowDown />
         </button>
    </div>
</div>