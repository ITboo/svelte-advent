<script lang="ts">
	import ChildrenList from '$lib/components/ChildrenList.svelte';
	import Header from '$lib/components/Header.svelte';
	import NewChild from '$lib/components/NewChild.svelte';
</script>

<svelte:boundary>
	<div class="app">
		<ChildrenList />
		{#snippet failed()}
			<p>fallback</p>
		{/snippet}
	</div>
</svelte:boundary>

<style>
	.app {
		width: 1200px;
		margin: 0 auto;
	}
</style>
