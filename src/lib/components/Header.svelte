<script>
	import { children } from "$lib/store/children.svelte";

	let username = '<strong>Elf #648290101</strong>';
</script>

<header class="header">
	<h1>HOHOHO Inc</h1>
    <a href="/">List</a>
    <a href="/register">Register Letter</a>
    <div class="">
	<p>Nice to meet you, {@html username}</p>
    <p>You have {children.length} entries</p>
</div>
</header>

<style>
    .header{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>
