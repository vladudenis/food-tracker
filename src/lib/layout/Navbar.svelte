<script>
	const navs = [
		{
			title: 'Home',
			href: '/'
		},
		{
			title: 'Nutrients',
			href: '/nutrients'
		},
		{
			title: 'Groceries',
			href: '/groceries'
		},
		{
			title: 'Inventory',
			href: '/inventory'
		},
	]

	// https://flowbite-svelte.com/docs/components/mega-menu
</script>

<nav>
	<div class="flex gap-4">
		<span>LOGO</span>
		<ul class="flex gap-2">
			{#each navs as {title, href}}
				<li>
					<a {href} {title}>
						{title}
					</a>
				</li>
			{/each}
		</ul>
	</div>
</nav>