<script lang="ts">
	// Types
	type Step = {
		id: number;
		title: string;
		description: string;
		imageSrc: string;
		imageAlt: string;
	};

	// Props
	let { className = '' }: { className?: string } = $props();

	// Static data for the steps.
	// This is kept inside the component for maintainability and to avoid over-abstraction with props.
	const steps: Step[] = [
		{
			id: 1,
			title: 'Capture Through Visual Recognition',
			description:
				'Simply perform a task on screen or with a camera. Squint’s AI observes and automatically captures every critical step.',
			imageSrc: 'https://www.ledr.com/colours/white.jpg',
			imageAlt: 'Visual of a process being recorded on a factory floor.'
		},
		{
			id: 2,
			title: 'Generate Instant Guides',
			description:
				'Squint instantly transforms your recording into a visual, step-by-step guide with annotations and clear instructions.',
			imageSrc: 'https://www.ledr.com/colours/white.jpg',
			imageAlt: 'An automatically generated step-by-step guide on a tablet.'
		},
		{
			id: 3,
			title: 'Deploy Across Your Operations',
			description:
				'Standardized instructions are instantly available to all team members, reducing new hire training time by 80% and ensuring consistent quality across shifts.',
			imageSrc: 'https://www.ledr.com/colours/white.jpg',
			imageAlt: 'A team member accessing a guide on a mobile device.'
		}
	];
</script>

<section class="bg-black py-24 text-white sm:py-32 {className}">
	<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
		<div class="mb-16">
			<div class="flex flex-col items-start justify-between lg:flex-row lg:items-end">
				<div class="max-w-3xl">
					<p class="font-body mb-2 font-mono text-sm uppercase text-neutral-400">How It Works</p>
					<h2 class="font-display text-4xl font-bold tracking-tight text-white sm:text-5xl">
						Capture Knowledge in 3 Simple Steps
					</h2>
				</div>
				<div class="mt-8 hidden shrink-0 lg:mt-0 lg:block">
					<a
						href="#"
						class="font-body inline-block rounded-lg bg-white px-8 py-4 text-lg font-semibold text-black shadow-sm transition hover:bg-neutral-200"
					>
						Request a Demo
					</a>
				</div>
			</div>
		</div>

		<div class="grid grid-cols-1 gap-8 lg:grid-cols-3">
			{#each steps as step (step.id)}
				<div class="flex flex-col overflow-hidden rounded-2xl bg-neutral-950">
					<div class="p-8">
						<p class="font-body mb-2 font-mono text-sm text-neutral-400">[{step.id}]</p>
						<h3 class="font-display mb-4 text-2xl font-semibold">{step.title}</h3>
						<p class="font-body text-lg text-neutral-300">{step.description}</p>
					</div>
					<div class="relative mt-auto flex-grow">
						<img
							src={step.imageSrc}
							alt={step.imageAlt}
							class="absolute inset-0 h-full w-full object-cover"
						/>
					</div>
				</div>
			{/each}
		</div>

		<div class="mt-12 text-center lg:hidden">
			<a
				href="#"
				class="font-body inline-block rounded-lg bg-white px-8 py-4 text-lg font-semibold text-black shadow-sm transition hover:bg-neutral-200"
			>
				Request a Demo
			</a>
		</div>
	</div>
</section>