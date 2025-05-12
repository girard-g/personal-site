<script lang="ts">
	import { initFlowbite } from 'flowbite';
	import { onMount } from 'svelte';

	const { links = [] } = $props();
	onMount(() => {
		initFlowbite();
	});
</script>

<!-- <header -->
<!-- 	class={`fixed z-50 w-full transition-all duration-300 ${scrolled ? 'bg-dark-400/90 shadow-md backdrop-blur-sm' : 'bg-transparent'}`} -->
<!-- > -->
<div class="container mx-auto px-4 sm:px-6 lg:px-8">
	<!-- <div class="flex items-center justify-between py-4"> -->
	<!-- 	<div class="flex items-center"> -->
	<!-- 	</div> -->

	<nav class="fixed start-0 top-0 z-20 w-full">
		<div class="mx-auto flex max-w-screen-xl flex-wrap items-center justify-between p-4">
			<a href="/" class="text-primary-500 text-2xl font-bold">
				Guillaume<span class="text-white">.Tech</span>
			</a>
			<div class="flex space-x-3 md:order-2 md:space-x-0 rtl:space-x-reverse">
				<!-- <button -->
				<!-- 	type="button" -->
				<!-- 	class="bg-primary-700 rounded-lg px-4 py-2 text-center text-sm font-medium text-white hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 focus:outline-none dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800" -->
				<!-- 	>Get started</button -->
				<!-- > -->
				<button
					data-collapse-toggle="navbar-sticky"
					type="button"
					class="inline-flex h-10 w-10 cursor-pointer items-center justify-center rounded-lg p-2 text-sm text-gray-500 hover:bg-gray-100 focus:ring-2 focus:ring-gray-200 focus:outline-none md:hidden dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
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
			<div class="hidden w-300 w-full items-center md:order-1 md:flex md:w-auto" id="navbar-sticky">
				<ul
					class="bg-dark-500 mt-4 flex flex-col rounded-lg p-4 font-medium md:mt-0 md:flex-row md:space-x-8 md:border-0 md:bg-white md:p-0 rtl:space-x-reverse"
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
