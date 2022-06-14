<script lang="ts">
	import Nav from '$lib/navigation.svelte';
	import '../app.css';
</script>

<svelte:head>
	
</svelte:head>
<main class="relative w-screen h-screen">
	<div class="-z-1 absolute top-0 inset-x-0 justify-center overflow-hidden pointer-events-none">
		<picture class="w-[108rem] flex-none inline-flex justify-end">
			<img src="/flare-effect.webp" alt="" class="w-[90rem] flex-none max-w-none block">
		</picture>
	</div>
	<Nav/>
	<slot />
</main>