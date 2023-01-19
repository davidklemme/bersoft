<script>
	import '../app.css';
	import Footer from '../../src/lib/Components/Footer.svelte';
</script>

<style>
	main {
		min-height: calc(100vh);
		min-width: max-content;
	}
	
	
</style>
<main id="FOO">
	<slot />
	
</main>
<Footer />	

