<script>
	let name = "Anton";
	let locationName = "KeyWest FL";
	let depth = 30;

	const addDepth = () => (depth += 1);
	const removeDepth = () => (depth -= 1);
	
</script>
<div class="container">
	<div class="card">
		<h1>{name}</h1>
		<h3>Location:{locationName}</h3>
		<h3>Depth:{depth}Ft</h3>
		<button class="btn" on:click={addDepth}>+1</button>
		<button class="btn btn-dark" on:click={removeDepth}>-1</button>
	</div>
</div>
<style>
	h1 {
		color: #333333;
	}
</style>