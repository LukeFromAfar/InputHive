<script>
	import Navbar  from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
	import "../app.css";
</script>

<svelte:head>
    <title>InputHive</title>
</svelte:head>

<div class="flex flex-col min-h-screen">
	<Navbar />

	<main class="flex-grow">
		{@render children()}
	</main>

	<Footer />

</div>