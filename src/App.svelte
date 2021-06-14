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
		},

	];
</script>
<Navbar />
<div class="container">
	<AddDiver />
	{#if divers.length === 0}
		<p>No Dives Today</p>
		{:else}
			{#each divers as diver}
				<Diver 
				name={diver.name}
				location={diver.location}
				depths={diver.depths} />
			{/each}
	{/if}
</div>