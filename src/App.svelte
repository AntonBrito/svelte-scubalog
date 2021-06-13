<script>
	import Navbar from "./Navbar.svelte";
	import Divers from "./Diver.svelte";
import Diver from "./Diver.svelte";

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