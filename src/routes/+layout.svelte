<script>
    import Nav from '../components/Nav.svelte'
    import Widgets from '../components/Widgets.svelte'
	import '../app.css';
</script>
<div class="flex flex-row">
    <Nav />
    <div class=" mx-auto max-h-screen  flex-1">
        <div class="grid grid-cols-10">
            <div class="col-span-10  lg:col-span-7 max-h-screen overflow-scroll scrollbar-hide border-r lg:justify-center flex ">
                <div class="lg:w-[70%] w-full px-5 lg:px-0 pt-10">

                    <slot></slot>
                </div>
            </div>
            <Widgets />
        </div>
    </div>
</div>

<style>
	.scrollbar-hide::-webkit-scrollbar {
		display: none;
	}
</style>
