<script lang="ts">
	import Carousseldenis from "$lib/components/Carousseldenis.svelte";
	import Contact from "$lib/components/Contact.svelte";
	import Download from "$lib/components/Download.svelte";
import Hero from "$lib/components/Hero.svelte";
 let image = [
	{title: "tuto-1" , src: "/assets/Heroe.jpg"},
	{title: "tuto-2" , src: "/assets/LogoGood.png"},
	{title: "tuto-2" , src: "/assets/logoapple.png"},
	{title: "tuto-2" , src: "/assets/logogoogle.png"},
	]
</script>

<section>
	<Hero/>
	<Carousseldenis/>
	<Download/>
	<Contact/>
</section>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Merriweather&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
</style>