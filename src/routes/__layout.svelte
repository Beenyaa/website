<script lang="ts">
	import Nav from '$lib/navigation.svelte';
	import '../app.css';
</script>

<svelte:head>
<!-- Primary Meta Tags -->
<title>Bence Gadányi | Full-Stack Engineer</title>
<meta name="title" content="Bence Gadányi | Full-Stack Engineer">
<meta name="description" content="Full-Stack Engineer @Equans - working on smart things.">

<!-- Open Graph / Facebook -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://bence.codes/">
<meta property="og:title" content="Bence Gadányi | Full-Stack Engineer">
<meta property="og:description" content="Full-Stack Engineer @Equans - working on smart things.">
<meta property="og:image" content="./preview.png">

<!-- Twitter -->
<meta property="twitter:card" content="summary_large_image">
<meta property="twitter:url" content="https://bence.codes/">
<meta property="twitter:title" content="Bence Gadányi | Full-Stack Engineer">
<meta property="twitter:description" content="Full-Stack Engineer @Equans - working on smart things.">
<meta property="twitter:image" content="./preview.png">

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