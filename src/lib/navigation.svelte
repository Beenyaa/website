<script lang="ts">
	import { page, navigating } from '$app/stores';
    let twist = 'rotate-0'
    let open = false
	
	function handleMouseClick() {
        if (open == false){
            twist = 'rotate-[135deg]';
            open = true
        }
        else{
            twist = 'rotate-0'
            open = false
        }
        
	}
</script>

<nav class="h-24 sm:h-32 flex items-center z-30 w-full">
    <div class="container mx-auto px-6 flex items-center justify-between">
        <div class="uppercase text-gray-800 dark:text-white font-black text-sm lg:flex items-center">
            <a href="/" class="py-2 px-6 flex hover:underline">
                {#if $page.url.pathname !== '/'}
                    ..
                {/if}
            </a>
        </div>
        <div class="flex items-center">
            <div class="font-sen text-gray-800 dark:text-white text-sm list-item lg:flex items-center hidden">
                <!-- <a href="/projects" class="py-2 px-6 flex hover:underline">
                    {#if $page.url.pathname !== '/projects'}
                    {#if $page.url.pathname == '/resume'}.{/if}./projects
                    {/if}
                    {#if $page.url.pathname == '/projects'}
                    .
                    {/if}
                </a> -->
                <a href="/resume" class="py-2 px-6 flex hover:underline">
                    {#if $page.url.pathname !== '/resume'}
                    {#if $page.url.pathname == '/projects'}.{/if}./resume
                    {/if}
                    {#if $page.url.pathname == '/resume'}
                    .
                    {/if}
                </a>
            </div>
            <button on:click={handleMouseClick} class="lg:hidden flex flex-col ml-4">
                <span class="ease-in duration-[125ms] {twist} text-4xl text-gray-800 dark:text-white mb-1">
                    +
                </span>
            </button>
        </div>
    </div>
</nav>