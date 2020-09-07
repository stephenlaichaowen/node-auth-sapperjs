<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';
	import Header from '../components/Header.svelte';	
</script>

<style>
	
</style>


<Header />
<main>
	<slot></slot>
</main>
<Footer />