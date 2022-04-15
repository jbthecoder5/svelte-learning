<script>
	import NavBar from "./Sections/Navbar.svelte"
	import VCard from "./Sections/VCard.svelte"
	import Form from "./UI/Form.svelte"

	let QRCode="";
	let values;
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
	<Form 
		bind:values
		on:createQRCode={e=>{
			QRCode=e.detail;
		}} />
		
	<VCard {values} {QRCode} />
</main>

