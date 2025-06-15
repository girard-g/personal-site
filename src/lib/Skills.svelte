<script lang="ts">
	import Skill from './Ui/skill.svelte';

	type Skill = {
		id: number;
		name: string;
		level: number; // Out of 100
	};

	const technicalSkills: Skill[] = [
		{ id: 0, name: 'Cloud Architecture', level: 95 },
		{ id: 1, name: 'System Design', level: 90 },
		{ id: 2, name: 'Data Engineering', level: 85 },
		{ id: 3, name: 'DevOps & CI/CD', level: 88 },
		{ id: 4, name: 'Cybersecurity', level: 82 },
		{ id: 5, name: 'AI & Machine Learning', level: 80 }
	];

	const leadershipSkills: Skill[] = [
		{ id: 0, name: 'Strategic Planning', level: 94 },
		{ id: 1, name: 'Team Leadership', level: 95 },
		{ id: 2, name: 'Project Management', level: 88 },
		{ id: 3, name: 'Stakeholder Management', level: 90 },
		{ id: 4, name: 'Technology Innovation', level: 95 },
		{ id: 5, name: 'Change Management', level: 85 }
	];

	const technologies = [
		'Rust',
		'AWS',
		'Sveltekit',
		'Docker',
		'PHP',
		'Symfony',
		'Terraform',
		'JavaScript',
		'TypeScript',
		'React',
		'Node.js',
		'PostgreSQL',
		'MongoDB',
		'MySQL',
		'Redis',
		'REST API',
		'CI/CD',
		'Git'
	];
</script>

<section id="skills" class="bg-dark-500 py-20">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="mx-auto mb-16 max-w-3xl text-center">
			<h2 class="mb-4 text-3xl font-bold text-white md:text-4xl">Skills & Expertise</h2>
			<div class="bg-primary-500 mx-auto mb-6 h-1 w-20"></div>
			<p class="text-lg text-gray-300">
				A combination of technical prowess and leadership capabilities that drive innovation
			</p>
		</div>

		<div class="grid gap-12 md:grid-cols-2">
			<div>
				<h3 class="mb-6 text-2xl font-semibold text-white">Technical Skills</h3>
				<div class="flex flex-wrap gap-4">
					{#each technicalSkills as skill (skill.id)}
						<Skill name={skill.name} />
					{/each}
				</div>
			</div>

			<div>
				<h3 class="mb-6 text-2xl font-semibold text-white">Leadership Skills</h3>
				<div class="flex flex-wrap gap-4">
					{#each leadershipSkills as skill (skill.id)}
						<Skill name={skill.name} />
					{/each}
				</div>
			</div>
		</div>

		<div class="mt-16">
			<h3 class="mb-6 text-center text-2xl font-semibold text-white">Technologies & Tools</h3>
			<div class="flex flex-wrap justify-center gap-3">
				{#each technologies as tech}
					<div
						class="bg-dark-300 border-dark-200 hover:border-primary-500 hover:text-primary-500 rounded-full border px-4 py-2 text-gray-300 transition-colors"
					>
						{tech}
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
