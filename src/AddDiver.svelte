<script>
  let diver = {
    name: "",
    location: "",
    depths: 0,
  }
</script>

<form class="grid-3">
  <input type="text" placeholder="Diver's Name" bind:value= {diver.name}>
  <input type="text" placeholder="Dive Location" bind:value= {diver.location}>
  <input type="number" placeholder="Dive Depth" bind:value= {diver.depths}>
  <input type="submit" class="btn btn-primary" value="Add Dive"> 
</form>