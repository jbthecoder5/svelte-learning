<script>
	import NavBar from "./Sections/Navbar.svelte"

	let disabled = false;
</script>

<NavBar title="vCard Generator" />

<button {disabled}>Reset</button>