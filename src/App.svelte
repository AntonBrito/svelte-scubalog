<script>
	let name = "Anton";
	let locationName = "KeyWest FL";
	let depths = 30;

	const addDepth = () => (depths += 1);
	const removeDepth = () => (depths -= 1);

</script>
<div class="container">
	<div class="card">
		<h1>{name}</h1>
		<h3>Location:{locationName}</h3>
		<h3>Depth:{depths}Ft</h3>
		<button class="btn" on:click={addDepth}>+1</button>
		<button class="btn btn-dark" on:click={removeDepth}>-1</button>
		<input type="number" bind:value={depths} />
	</div>
</div>
<style>
	h1 {
		color: #333333;
	}

	h3 {
		margin-bottom: 10px;;
	}
</style>