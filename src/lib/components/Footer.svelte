<script lang="ts">
	// Props
	let { className = '' }: { className?: string } = $props();

	// Types for structured data
	type FooterLink = {
		href: string;
		text: string;
	};

	type FooterColumn = {
		title: string;
		links: FooterLink[];
	};

	type SocialLink = {
		name: string;
		href: string;
		iconPath: string;
	};

	// Static data for footer navigation links. This improves maintainability.
	const footerColumns: FooterColumn[] = [
		{
			title: 'Platform',
			links: [
				{ href: '#', text: 'Visual Recognition' },
				{ href: '#', text: 'Work Instructions' },
				{ href: '#', text: 'Knowledge Capture' },
				{ href: '#', text: 'Security' }
			]
		},
		{
			title: 'Solutions',
			links: [
				{ href: '#', text: 'Manufacturing' },
				{ href: '#', text: 'Training & Onboarding' },
				{ href: '#', text: 'Process Standardization' },
				{ href: '#', text: 'Tribal Knowledge' }
			]
		},
		{
			title: 'Resources',
			links: [
				{ href: '#', text: 'Case Studies' },
				{ href: '#', text: 'ROI Calculator' },
				{ href: '#', text: 'Implementation Guide' },
				{ href: '#', text: 'Support' }
			]
		}
	];

	// Static data for social media icons and links.
	const socialLinks: SocialLink[] = [
		{
			name: 'Twitter',
			href: '#',
			iconPath:
				'M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z'
		},
		{
			name: 'LinkedIn',
			href: '#',
			iconPath:
				'M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z'
		}
	];

	// Dynamically get the current year for the copyright notice.
	const currentYear = new Date().getFullYear();
</script>

<footer class={`bg-black ${className}`}>
	<div class="mx-auto max-w-screen-xl px-4 py-16 sm:px-6 lg:px-8">
		<div class="flex flex-col gap-12 lg:flex-row lg:items-start lg:justify-between">
			<a href="#" class="font-display text-2xl font-bold text-white">Squint</a>
			<div
				class="font-body grid w-full grid-cols-2 gap-8 text-sm text-neutral-400 sm:grid-cols-3 lg:w-auto"
			>
				{#each footerColumns as column}
					<div class="flex flex-col gap-y-3">
						<h3 class="font-display mb-1 font-semibold text-white">{column.title}</h3>
						{#each column.links as link}
							<a href={link.href} class="transition hover:text-white">{link.text}</a>
						{/each}
					</div>
				{/each}
			</div>
		</div>
		<div
			class="font-body mt-12 flex flex-col items-center justify-between gap-6 border-t border-neutral-800 pt-8 sm:flex-row"
		>
			<p class="text-sm text-neutral-400">Copyright © {currentYear} Squint</p>
			<div class="flex items-center gap-x-3 text-sm">
				<a href="#" class="text-neutral-400 transition hover:text-white">Terms of Service</a>
				<span class="text-neutral-600">|</span>
				<a href="#" class="text-neutral-400 transition hover:text-white">Privacy Policy</a>
			</div>
			<div class="flex items-center gap-x-4">
				{#each socialLinks as social}
					<a href={social.href} class="text-neutral-400 transition hover:text-white">
						<span class="sr-only">{social.name}</span>
						<svg class="h-5 w-5 fill-current" viewBox="0 0 24 24" aria-hidden="true">
							<path d={social.iconPath} />
						</svg>
					</a>
				{/each}
			</div>
		</div>
	</div>
</footer>