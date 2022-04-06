<script>
	import NavBar from "./Sections/Navbar.svelte"

	let disabled = true;

	function keyPressed() {
		disabled = false
	}

	function resetClicked() {
		disabled = true;
	}
</script>

<NavBar title="vCard Generator" />

<form>
	<label>Name 
		<input type="text" placeholder="Please enter your name"
		on:keydown={keyPressed} />
	</label>
	<button type="reset" {disabled} on:click={resetClicked}>Reset</button>
</form>