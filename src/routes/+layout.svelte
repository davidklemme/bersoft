<script>
	import '../app.css';
	import Footer from '../../src/lib/Components/Footer.svelte';
</script>

<style>
	main {
		min-height: calc(100vh);
		min-width: max-content;
	}
	.footer {
		position: fixed;
		bottom: 0;
		width: 100vh;
	}
</style>
<main id="FOO">
	<slot />
	<Footer />	
</main>


