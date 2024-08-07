<script>
	const navs = [
		{
			title: 'Demo',
			href: '#demo'
		},
		{
			title: 'Pricing',
			href: '#pricing'
		},
		{
			title: 'Testimonials',
			href: '#testimonials'
		},
	]
</script>

<nav>
	<div class="flex gap-16 bg-emerald-500 py-4 px-6 rounded-xl text-white font-bold text-xl">
		<a href="/static">
			<span>LOGO</span>
		</a>
		<ul class="flex gap-12">
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