<script>
	import '../app.css';
	import Footer from '../../src/lib/Components/Footer.svelte';
	import SlideOver from '$lib/Components/SlideOver.svelte';
</script>

<style>
	main {
		min-height: calc(90vh);
		min-width: calc(90vw);
	}
	
	
</style>
<main class="">
	<slot />
	
</main>
<Footer />	

