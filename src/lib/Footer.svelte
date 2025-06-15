<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="bg-dark-900 py-12 text-white">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex flex-col items-center justify-between md:flex-row">
			<div class="mb-6 md:mb-0">
				<a href="#" class="text-primary-400 text-2xl font-bold">
					Guillaume<span class="text-white">.Tech</span>
				</a>
				<p class="mt-2 max-w-md text-gray-400">
					Driving digital transformation through innovative technology solutions and strategic
					leadership.
				</p>
			</div>
			<div class="flex flex-col items-center md:items-end">
				<div class="mb-4 flex gap-4">
					<a
						target="_blank"
						href="https://linkedin.com/in/guillaumegirardwebdev"
						class="hover:text-primary-400 text-gray-400 transition-colors"
					>
						LinkedIn
					</a>
					<a
						target="_blank"
						href="https://github.com/girard-g"
						class="hover:text-primary-400 text-gray-400 transition-colors"
					>
						GitHub
					</a>
					<!-- <a href="#" class="hover:text-primary-400 text-gray-400 transition-colors"> Twitter </a> -->
				</div>
				<p class="text-sm text-gray-500">
					© {currentYear} Guillaume Girard. All rights reserved.
				</p>
			</div>
		</div>
	</div>
</footer>
