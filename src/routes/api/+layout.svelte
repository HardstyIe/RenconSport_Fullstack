<script lang="ts">
	import Footer from '$lib/Navbar.svelte';
	import Navbar from '$lib/Footer.svelte';
</script>

<main>
	<Navbar />
<!--	slot = "body" -->
	<slot
	/>
	<Footer />
</main>
