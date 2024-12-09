<script>
	import { children } from '$lib/store/children.svelte';

	export function addChild(child) {
		children.unshift(child);
	}
	let name = $state('');
	let tally = $state();
	function onsubmit(event) {
		event.preventDefault();
		if (!name) return;
		addChild({
			name,
			tally,
			id: Date.now()
		});
		name = '';
		tally = '';
	}
</script>

<form {onsubmit}>
	<input type="text" bind:value={name} required/>
	<input type="text" bind:value={tally} required/>
	<button disabled={!name}>Add</button>
</form>
