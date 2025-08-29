<script lang="ts">
	// Props
	let { className = '' }: { className?: string } = $props();

	// Types for logo data
	type Logo = {
		src: string;
		alt: string;
	};

	// Static data for client logos.
	// Using a constant array as the data doesn't change.
	// This keeps the template clean and maintainable.
	const logos: Logo[] = [
		{ src: 'https://logo.clearbit.com/caterpillar.com', alt: 'Caterpillar' },
		{ src: 'https://logo.clearbit.com/boeing.com', alt: 'Boeing' },
		{ src: 'https://logo.clearbit.com/ge.com', alt: 'General Electric' },
		{ src: 'https://logo.clearbit.com/honeywell.com', alt: 'Honeywell' },
		{ src: 'https://logo.clearbit.com/siemens.com', alt: 'Siemens' }
	];
</script>

<section class={`py-16 ${className}`}>
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center">
			<p class="font-body text-base font-semibold text-gray-400">
				TRUSTED BY OPERATIONS TEAMS AT COMPANIES LIKE
			</p>
		</div>
		<div
			class="relative mt-8 flex overflow-x-hidden [mask-image:linear-gradient(to_right,transparent,black_5%,black_95%,transparent)]"
		>
			<!-- The logos are duplicated to create a seamless scrolling marquee effect -->
			<div class="flex shrink-0 animate-marquee items-center">
				{#each logos as logo}
					<div class="p-5">
						<img class="h-auto w-32" src={logo.src} alt={logo.alt} />
					</div>
				{/each}
			</div>
			<div class="flex shrink-0 animate-marquee items-center" aria-hidden="true">
				{#each logos as logo}
					<div class="p-5">
						<img class="h-auto w-32" src={logo.src} alt={logo.alt} />
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>