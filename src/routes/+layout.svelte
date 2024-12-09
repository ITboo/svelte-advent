<script>
	import Header from '$lib/components/Header.svelte';
	let { children } = $props();
</script>

<Header />
<main class="main">
	{@render children()}
	<div class="aside">Aside content</div>
</main>

<style>
	.main {
		display: flex;
		justify-content: space-between;
	}
</style>
