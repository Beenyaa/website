<script lang="ts">
	import { page, navigating } from '$app/stores';
</script>

<header class="h-24 sm:h-32 flex items-center z-30 w-full">
    <div class="container mx-auto px-6 flex items-center justify-between">
        <div class="uppercase text-gray-800 dark:text-white font-black text-sm lg:flex items-center">
            <a href="/" class="py-2 px-6 flex hover:underline">
                {#if $page.url.pathname !== '/'}
                    ..
                {/if}
            </a>
        </div>
        <div class="flex items-center">
            <nav class="font-sen text-gray-800 dark:text-white text-sm lg:flex items-center hidden">
                <a href="/projects" class="py-2 px-6 flex hover:underline">
                    {#if $page.url.pathname !== '/projects'}
                    /projects
                    {/if}
                    {#if $page.url.pathname == '/projects'}
                    .
                    {/if}
                </a>
                <a href="/resume" class="py-2 px-6 flex hover:underline">
                    {#if $page.url.pathname !== '/resume'}
                    /resume
                    {/if}
                    {#if $page.url.pathname == '/resume'}
                    .
                    {/if}
                </a>
                <!-- <a href="/about" class="py-2 px-6 flex hover:underline">
                    {#if $page.url.pathname !== '/about'}
                    /about
                    {/if}
                    {#if $page.url.pathname == '/about'}
                    .
                    {/if}
                </a>
                <a href="#" class="hidden py-2 px-6 flex hover:underline">
                    ./contact
                </a> -->
            </nav>
            <button class="lg:hidden flex flex-col ml-4">
                <span class="w-6 h-1 bg-gray-800 dark:bg-white mb-1">
                </span>
                <span class="w-1 h-6 bg-gray-800 dark:bg-white mb-1">
                </span>
            </button>
        </div>
    </div>
</header>