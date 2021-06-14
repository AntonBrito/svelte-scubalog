<script>
	import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

	export let name;
	export let location;
	export let depths;
	let showControls = false

	const addDepth = () => (depths += 1);
	const removeDepth = () => (depths -= 1);
	const toggleControls = () => (showControls = !showControls); 
	const onDelete = () => dispatch("removeDiver", name);
</script>
	<div class="card">
		<h1>{name}</h1>
		<button class="btn btn-sm" on:click={toggleControls}>
			{#if showControls}-{:else}+{/if}
		</button> 
		<button class="btn btn-danger btn-sm" on:click={onDelete}>x</button>
		<h3>Location:{location}</h3>
		<h3>Depth:{depths}Ft</h3>
		{#if showControls}
		<button class="btn" on:click={addDepth}>+1</button>
		<button class="btn btn-dark" on:click={removeDepth}>-1</button>
		<input type="number" bind:value={depths} />
		{/if}
	</div>
<style>
	h1 {
		color: #333333;
	}

	h3 {
		margin-bottom: 10px;;
	}
</style>