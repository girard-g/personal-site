<script lang="ts">
	type Experience = {
		id: number;
		title: string;
		company: string;
		period: string;
		description: string;
	};
	const experiences: Experience[] = [
		{
			id: 0,
			title: 'CTO',
			company: 'Gaia Software',
			period: '2019 - Present',
			description:
				'Leading the technology strategy and digital transformation initiatives. Managing a team of 50+ engineers across multiple departments. Implemented cloud migration strategy resulting in 40% cost reduction and improved scalability.'
		},
		{
			id: 1,
			title: 'CTO',
			company: 'Grytics',
			period: '2015 - 2019',
			description:
				"Oversaw the development of the company's flagship data processing platform. Scaled the engineering team from 10 to 35. Established DevOps practices and reduced deployment time by 70%."
		},
		{
			id: 2,
			title: 'Lead Developer',
			company: 'Grytics',
			period: '2011 - 2015',
			description:
				"Designed and implemented microservices architecture for the company's core products. Led the adoption of container technologies and orchestration platforms. Mentored junior developers and established coding standards."
		},
		{
			id: 3,
			title: 'Backend Developer',
			company: 'Grytics',
			period: '2015 - 2011',
			description:
				'Headed the development of client-facing web applications and internal tools. Introduced test-driven development practices. Collaborated with UX/UI designers to improve user experiences.'
		}
	];
</script>

<section id="experience" class="bg-dark-400 py-20">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="mx-auto mb-16 max-w-3xl text-center">
			<h2 class="mb-4 text-3xl font-bold md:text-4xl">Professional Experience</h2>
			<div class="bg-primary-500 mx-auto mb-6 h-1 w-20"></div>
			<p class="text-lg text-gray-300">
				A career journey building and leading technology solutions
			</p>
		</div>

		<div class="mx-auto max-w-4xl">
			<div class="border-dark-200 relative ml-3 border-l-2">
				{#each experiences as exp (exp.id)}
					<div
						class="bg-primary-500 border-dark-400 absolute -left-3 h-6 w-6 rounded-full border-4"
					></div>
					<div class="bg-dark-300 rounded-lg p-6 shadow-md transition-shadow hover:shadow-lg">
						<div class="mb-2 flex flex-wrap justify-between">
							<h3 class="text-xl font-semibold text-white">{exp.title}</h3>
							<span
								class="bg-primary-500/20 text-primary-400 rounded-full px-3 py-1 text-sm font-medium"
							>
								{exp.period}
							</span>
						</div>
						<h4 class="text-primary-500 mb-4 font-medium">{exp.company}</h4>
						<p class="text-gray-300">{exp.description}</p>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
