<script lang="ts">
	// This component is static and does not require any reactive state or logic.
	// It's designed for displaying security and compliance information.

	// Props
	let { className = '' }: { className?: string } = $props();
</script>

<section class="py-16 sm:py-24 bg-[var(--color-background)] {className}">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="max-w-4xl mx-auto text-center">
			<h2 class="text-4xl font-bold tracking-tight sm:text-5xl font-display text-neutral-50">
				Enterprise-Grade Security You Can Trust
			</h2>
			<p class="mt-6 text-lg leading-8 text-neutral-300 font-body">
				Squint is built with robust security and data privacy standards to protect your proprietary
				manufacturing processes and intellectual property.
			</p>
		</div>
		<div class="mt-16">
			<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2">
				<div class="border-b border-r-0 border-neutral-800 p-8 md:border-r">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="w-8 h-8 mb-6 text-neutral-400"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M16.5 10.5V6.75a4.5 4.5 0 1 0-9 0v3.75m-.75 11.25h10.5a2.25 2.25 0 0 0 2.25-2.25v-6.75a2.25 2.25 0 0 0-2.25-2.25H6.75a2.25 2.25 0 0 0-2.25 2.25v6.75a2.25 2.25 0 0 0 2.25 2.25Z"
						/>
					</svg>
					<h3 class="text-xl font-semibold font-display text-neutral-50">Data Encryption</h3>
					<p class="mt-2 text-neutral-400 font-body">
						All data, both in transit and at rest, is encrypted using industry-standard protocols to
						protect your sensitive process information.
					</p>
				</div>
				<div class="border-b border-r-0 border-neutral-800 p-8 md:border-r-0">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="w-8 h-8 mb-6 text-neutral-400"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M9 12.75 11.25 15 15 9.75m-3-7.036A11.959 11.959 0 0 1 3.598 6 11.99 11.99 0 0 0 3 9.749c0 5.592 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.31-.21-2.571-.598-3.751h-.152c-3.196 0-6.1-1.248-8.25-3.286Zm-1.5 6.036a.75.75 0 0 1-1.5 0v-1.5a.75.75 0 0 1 1.5 0v1.5Z"
						/>
					</svg>
					<h3 class="text-xl font-semibold font-display text-neutral-50">SOC 2 Compliant</h3>
					<p class="mt-2 text-neutral-400 font-body">
						Our platform meets SOC 2 Type II compliance standards, ensuring your manufacturing data remains secure, available, and confidential at all times.
					</p>
				</div>
				<div class="border-b border-r-0 border-neutral-800 p-8 md:border-b-0 md:border-r">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="w-8 h-8 mb-6 text-neutral-400"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M15 19.128a9.38 9.38 0 0 0 2.625.372 9.337 9.337 0 0 0 4.121-2.308l.247-2.477a6.375 6.375 0 0 0-6.375-6.375H7.5a6.375 6.375 0 0 0-6.375 6.375v2.477A9.337 9.337 0 0 0 5.25 19.5a9.38 9.38 0 0 0 2.625-.372M15 19.128v-3.86a6.375 6.375 0 0 0-3.75-5.941c-1.356-.667-3.114-.667-4.5 0A6.375 6.375 0 0 0 3 15.268v3.86M15 19.128c-1.355.667-3.114.667-4.5 0"
						/>
					</svg>
					<h3 class="text-xl font-semibold font-display text-neutral-50">
						Role-Based Access Control
					</h3>
					<p class="mt-2 text-neutral-400 font-body">
						Granular, role-based access controls ensure that only authorized personnel can view or
						edit specific work instructions.
					</p>
				</div>
				<div class="p-8">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="w-8 h-8 mb-6 text-neutral-400"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M12 21a9.004 9.004 0 0 0 8.716-6.747M12 21a9.004 9.004 0 0 1-8.716-6.747M12 21c2.485 0 4.5-4.03 4.5-9S14.485 3 12 3m0 18c-2.485 0-4.5-4.03-4.5-9S9.515 3 12 3m0 0a8.997 8.997 0 0 1 7.843 4.582M12 3a8.997 8.997 0 0 0-7.843 4.582m15.686 0A11.953 11.953 0 0 1 12 10.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0 1 21 12c0 .778-.099 1.533-.284 2.253m0 0A11.953 11.953 0 0 1 12 13.5c-2.998 0-5.74-1.1-7.843-2.918m15.686 0A8.959 8.959 0 0 1 21 12"
						/>
					</svg>
					<h3 class="text-xl font-semibold font-display text-neutral-50">
						Secure Cloud Infrastructure
					</h3>
					<p class="mt-2 text-neutral-400 font-body">
						We leverage leading cloud providers with world-class security practices to host our
						services and your data.
					</p>
				</div>
			</div>
		</div>
	</div>
</section>