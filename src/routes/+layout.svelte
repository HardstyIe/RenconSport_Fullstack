<script lang="ts">
	import Footer from '../lib/Footer.svelte';
	import Navbar from '../lib/Navbar.svelte';
</script>

<main>
	<Navbar />
	<slot />
	<Footer />
</main>
