<script lang="ts">

	import Footer from '../lib/Footer.svelte';
	import Navbar from '../lib/Navbar.svelte';
	

</script>

<main>
	<Navbar />
	<slot />
	
	<!-- Tout ce qui se trouve dans slot je le code dans +page.svelte (c'est le body) -->
	<Footer />
</main>
