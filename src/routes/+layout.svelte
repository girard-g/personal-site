<script lang="ts">
	import Navigation from '$lib/Navigation.svelte';
	import '../app.css';

	let { children } = $props();
	let links = [
		{ id: 0, href: '/', label: 'Home' },
		{ id: 1, href: '#about', label: 'About' },
		{ id: 2, href: '#skills', label: 'Skillz' },
		{ id: 3, href: '#experience', label: 'Experience' },
		{ id: 4, href: '#contact', label: 'Contact' }
	];
</script>

<div class="from-dark-500 to-dark-400 bg-gradient-to-br">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<Navigation {links} />
		{@render children()}
	</div>
</div>
