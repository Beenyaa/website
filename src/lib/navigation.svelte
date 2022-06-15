<script lang="ts">
	import { page, navigating } from '$app/stores';
    let twist = 'rotate-0'
    let open = "hidden"
	
	function handleMouseClick() {
        if (open == "hidden"){
            twist = 'rotate-[135deg]';
            open = ""
        }
        else{
            twist = 'rotate-0'
            open = "hidden"
        }
        
	}

    function closeNavigation() {
        twist = 'rotate-0'
        open = "hidden"
        
	}
</script>

<nav class="h-24 sm:h-32 flex items-center z-30 w-full">
    <div class="container mx-auto px-6 flex items-center justify-between">
        <div class="uppercase text-gray-800 dark:text-white font-black text-sm lg:flex items-center">
            <a href="/" class="z-100 py-2 px-6 flex hover:underline" on:click={closeNavigation}>
                {#if $page.url.pathname !== '/'}
                    ..
                {/if}
            </a>
        </div>
        <div class="flex items-center">
            <div class="z-20 absolute inset-0 justify-center dark:bg-gradient-to-u dark:from-gray-900 dark:to-slate-900 bg-gradient-to-r from-gray-100 to-slate-100 w-full h-screen font-sen text-gray-800 dark:text-white text-sm flex flex-col lg:relative lg:flex-row items-center {open} lg:flex lg:bg-none">
                <!-- <a href="/projects" class="py-2 px-6 flex hover:underline" on:click={closeNavigation}>
                    {#if $page.url.pathname !== '/projects'}
                    {#if $page.url.pathname == '/resume'}.{/if}./projects
                    {/if}
                    {#if $page.url.pathname == '/projects'}
                    .
                    {/if}
                </a> -->
                <a href="/resume" class="py-2 px-6 flex hover:underline" on:click={closeNavigation}>
                    {#if $page.url.pathname !== '/resume'}
                    {#if $page.url.pathname == '/projects'}.{/if}./resume
                    {/if}
                    {#if $page.url.pathname == '/resume'}
                    .
                    {/if}
                </a>
            </div>
            <button on:click={handleMouseClick} class="lg:hidden flex flex-col ml-4">
                <span class="z-20 ease-in duration-[125ms] {twist} text-4xl text-gray-800 dark:text-white mb-1">
                    +
                </span>
            </button>
        </div>
    </div>
</nav>