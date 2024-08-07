<script>
	import "../app.css";
	import Navbar from '$lib/Navbar.svelte';

	// Hide footer if not on landing page and switch between Navbar and LandingNavbar
	// Calculate slot height based on presence/absence of footer component with calc()
</script>

<div class="h-full w-full flex flex-col items-center">
	<Navbar />
	<slot />
</div>