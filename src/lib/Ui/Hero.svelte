<script lang="ts">
	import Briefcase from './icons/Briefcase.svelte';
	import Envelope from './icons/envelope.svelte';
	import User from './icons/User.svelte';
</script>

<section id="hero" class="flex min-h-screen items-center pt-16">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid items-center gap-8 md:grid-cols-2">
			<div class="order-2 md:order-1">
				<h1 class="mb-4 text-4xl leading-tight font-bold md:text-5xl">
					<span class="text-white">Guillaume Girard</span>
					<span class="text-primary-500 block">Freelance</span>
				</h1>
				<div class="mb-6 flex flex-col gap-8">
					<p class="max-w-lg text-xl text-gray-300">
						Driving digital transformation through innovative technology solutions and strategic
						leadership.
					</p>
					<div class="space-y-4 pt-4">
						<div class="flex items-center gap-4">
							<div class="bg-primary-500/20 text-primary-500 rounded-full p-3">
								<User />
							</div>
							<div>
								<h4 class="text-secondary-500 font-medium">Name</h4>
								<p class="text-gray-300">Guillaume Girard</p>
							</div>
						</div>
						<div class="flex items-center gap-4">
							<div class="bg-primary-500/20 text-primary-500 rounded-full p-3">
								<Briefcase />
							</div>
							<div>
								<h4 class="text-secondary-500 font-medium">Role</h4>
								<p class="text-gray-300">CTO - LEAD - DEV</p>
							</div>
						</div>
						<div class="flex items-center gap-4">
							<div class="bg-primary-500/20 text-primary-500 rounded-full p-3">
								<Envelope />
							</div>
							<div>
								<h4 class="text-secondary-500 font-medium">Email</h4>
								<p class="text-gray-300">guillaumegirardpro@gmail.com</p>
							</div>
						</div>
					</div>
				</div>
				<div class="flex flex-wrap gap-4">
					<button
						class="bg-primary-500 hover:bg-primary-600 flex cursor-pointer items-center gap-2 rounded-md px-6 py-3 font-medium text-white transition-colors"
					>
						Get in Touch
						<!--TODO: Add icon here-->
						<!-- <ArrowRight size={18} /> -->
					</button>
					<a
						href="#about"
						class="hover:border-primary-500 hover:text-primary-500 border-primary-500 rounded-md border px-6 py-3 font-medium text-gray-300 transition-colors"
					>
						Learn More
					</a>
				</div>
			</div>
			<div class="order-1 flex justify-center md:order-2 md:justify-end">
				<div class="relative">
					<div
						class="bg-primary-500/20 flex h-64 w-64 items-center justify-center rounded-full md:h-80 md:w-80"
					>
						<div
							class="from-primary-400 to-primary-600 flex h-56 w-56 items-center justify-center rounded-full bg-gradient-to-br text-4xl font-bold text-white opacity-90 md:h-72 md:w-72"
						>
							GG
						</div>
					</div>
					<div class="bg-dark-300 absolute -right-2 -bottom-2 rounded-lg p-3 shadow-lg">
						<span class="text-primary-500 font-semibold"
							><span class="text-secondary-500">10+</span> Years in Tech</span
						>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
