<script lang="ts">
	import { initFlowbite } from 'flowbite';
	import { onMount } from 'svelte';

	const { links = [] } = $props();

	let scrolled = $state(false);

	function handleScroll() {
		if (window.scrollY > 0) {
			scrolled = true;
		} else {
			scrolled = false;
		}
	}

	onMount(() => {
		initFlowbite();
		window.addEventListener('scroll', handleScroll);
	});
</script>

<div class="container mx-auto bg-green-500 px-4 sm:px-6 lg:px-8">
	<nav
		class={`fixed start-0 top-0 z-20 w-full transition-all duration-300 sm:px-6 lg:px-8 ${scrolled ? 'bg-dark-500/90 shadow-xl backdrop-blur-sm' : 'bg-transparent'}`}
	>
		<div class="mx-auto flex max-w-screen-xl flex-wrap items-center justify-between p-4">
			<a href="/" class="text-primary-500 text-2xl font-bold">
				Guillaume<span class="text-white">.Tech</span>
			</a>
			<div class="flex space-x-3 md:order-2 md:space-x-0 rtl:space-x-reverse">
				<button
					class="bg-primary-500 hover:bg-primary-600 flex cursor-pointer items-center gap-2 rounded-md px-4 py-2 text-sm font-medium text-white transition-colors"
				>
					Get in Touch
					<!--TODO: Add icon here-->
					<!-- <ArrowRight size={18} /> -->
				</button>
				<button
					data-collapse-toggle="navbar-sticky"
					type="button"
					class="inline-flex h-10 w-10 items-center justify-center rounded-lg p-2 text-sm text-gray-500 hover:bg-gray-100 focus:ring-2 focus:ring-gray-200 focus:outline-none md:hidden dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
					aria-controls="navbar-sticky"
					aria-expanded="false"
				>
					<span class="sr-only">Open main menu</span>
					<svg
						class="h-5 w-5"
						aria-hidden="true"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 17 14"
					>
						<path
							stroke="currentColor"
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M1 1h15M1 7h15M1 13h15"
						/>
					</svg>
				</button>
			</div>
			<div
				class="hidden w-full items-center justify-between md:order-1 md:flex md:w-auto"
				id="navbar-sticky"
			>
				<ul
					class="mt-4 flex flex-col rounded-lg border border-gray-100 bg-transparent p-4 font-medium md:mt-0 md:flex-row md:space-x-8 md:border-0 md:p-0 rtl:space-x-reverse"
				>
					{#each links as link (link.id)}
						<li>
							<a
								href={link.href}
								class="hover:text-primary-500 block rounded-sm px-3 py-2 text-white md:bg-transparent md:p-0"
								aria-current="page">{link.label}</a
							>
						</li>
					{/each}
				</ul>
			</div>
		</div>
	</nav>
</div>
<!-- </header> -->
