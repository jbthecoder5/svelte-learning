<script>
	import NavBar from "./Sections/Navbar.svelte"
	import Form from "./UI/Form.svelte"
	import vCard from "./Sections/VCard.svelte"

	let QRCode="";
</script>

<style>
	main {
		padding: 1rem;
		max-width: 600px;
		margin: 0 auto;
	}
</style>

<NavBar title="vCard Generator" />

<main>
	<Form on:CreateQRCode={e=>{QRCode=e.detail;}} />

	<VCard {QRCode} />
</main>

