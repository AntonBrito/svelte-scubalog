<script>
	import Navbar from "./Navbar.svelte";
	import Diver from "./Diver.svelte";
  import AddDiver from "./AddDiver.svelte";

	let divers = [
		{
			name: "Anton",
			location: "KeyWest, FL",
			depths: 12,
		},
		{
			name: "Riley",
			location: "Jamestown, RI",
			depths: 20,
		},
		{
			name: "Belmas",
			location: "QuebraCanela, CapeVerde",
			depths: 12,
		}
	];
	const addDiver = (e) => {
		const newDiver = e.detail;
		divers = [...divers, newDiver];
	}

	const removeDiver = (e) => {
		divers = divers.filter(diver => diver.name !== e.detail)
	}
</script>

<Navbar />
<div class="container">
	<AddDiver on:adddiver={addDiver}/>
	{#if divers.length === 0}
		<p>No Dives Today</p>
		{:else}
			{#each divers as diver}
				<Diver 
				name={diver.name}
				location={diver.location}
				depths={diver.depths} 
				on:removeDiver={removeDiver} 
				/>
			{/each}
	{/if}
</div>