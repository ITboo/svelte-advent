<script>
	import { children } from "$lib/store/children.svelte";
</script>

<div class="list">
{#if children.length===0}
    <p>No children. Take a coffee, bro</p>
{/if}  
{#each children as child}
	<div class="card">
		<h2>{child.name}</h2>
		{#if child.tally >= 0}
			<span class="nice">Nice</span>
		{:else if child.tally < 0}
			<span class="naughty">Naughty</span>
		{:else}
			<span class="no_data">No data</span>
		{/if}
	</div>
{/each}
</div>

<style>
    .list{
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
	.nice {
		color: green;
	}
	.naughty {
		color: red;
	}
	.no_data {
		color: gray;
	}
	.card {
		display: flex;
		align-items: center;
		gap: 20px;
		padding: 5px;
		border: 1px solid gray;
        border-radius: 10px;
        width: 400px;
	}
</style>
