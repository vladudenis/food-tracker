<script>
	import { page } from '$app/stores';
	import { UserCircleOutline } from 'flowbite-svelte-icons';

	$: currentPage = $page.url.pathname
	let navs = [
		{
			title: 'Nutrients',
			href: '/nutrients',
		},
		{
			title: 'Groceries',
			href: '/groceries',
		},
		{
			title: 'Inventory',
			href: '/inventory',
		},
		{
			title: 'Recipes',
			href: '/recipes',
		},
	]
</script>

<style>
    .hover-underline-animation {
        @apply inline-block relative;
    }

    .hover-underline-animation::after {
        @apply bg-black content-[''] absolute w-full scale-x-0 h-[2px] bottom-0 left-0 origin-left transition-all ease-in-out duration-300;
    }

    .hover-underline-animation:hover::after,
    .hover-underline-animation.active::after{
        @apply scale-x-100;
    }
</style>

<nav class="w-full">
	<div class="w-full flex justify-between gap-12 py-20 px-36 uppercase text-xl">
		<a href="/">
			<span>LOGO</span>
		</a>
		<ul class="flex gap-8">
			{#each navs as {title, href}}
				<li>
					<a {href} class={`hover-underline-animation`}
						 class:active={currentPage === href}
					>
						{title}
					</a>
				</li>
			{/each}
			<UserCircleOutline size="xl" ariaLabel="user circle outline icon" class="ml-12" />
		</ul>
	</div>
</nav>