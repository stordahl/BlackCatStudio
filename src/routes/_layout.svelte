<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';

	export let segment;
</script>

<style>
:root {
		--bg: #E0DCD8;
		--light-orange: #DDA788;
		--dark-orange:#BB5215;
		--light-blue:#E6F2FF;
		--dark-blue:#A5C4E7;
		--light-green: #999E90;
		--dark-green:#4E563E;
		--black:#1F1F1F;
	}
	main {
		position: relative;
		max-width: 56em;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
		display:grid;
	}
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>

<Footer />