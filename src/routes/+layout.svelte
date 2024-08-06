<script>
	import "../app.css";
	import Navbar from '$lib/layout/Navbar.svelte';
	import Footer from '$lib/layout/Footer.svelte';

	// Hide footer if not on landing page
	// Calculate slot height based on presence/absence of footer component with calc()
</script>

<div class="h-full w-full flex flex-col items-center">
	<Navbar />
	<slot />
	<Footer />
</div>