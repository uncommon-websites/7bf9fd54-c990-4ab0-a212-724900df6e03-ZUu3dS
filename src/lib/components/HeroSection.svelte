<script lang="ts">
	// Props for allowing external class overrides
	let { className = '' }: { className?: string } = $props();
</script>

<section class="bg-[var(--color-background)] py-24 text-white sm:py-32 {className}">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="mx-auto flex max-w-4xl flex-col items-center text-center">
			<h1 class="font-display text-5xl font-bold tracking-tight text-white sm:text-7xl">
				Instantly Document Any Manufacturing Process.
			</h1>
			<h3 class="font-body mt-6 max-w-3xl text-xl font-light text-gray-200 sm:text-2xl">
				Squint uses visual recognition to turn complex workflows into simple, step-by-step guides,
				eliminating outdated manuals and lost knowledge.
			</h3>
			<div
				class="mt-10 flex w-full flex-col items-center justify-center gap-4 sm:w-auto sm:flex-row sm:gap-8"
			>
				<a
					href="#"
					class="font-body w-full rounded-md border border-white px-8 py-3 text-center text-base font-semibold text-white shadow-sm transition-colors hover:bg-white hover:text-black sm:w-auto"
				>
					Sign In
				</a>
				<a
					href="#"
					class="font-body group inline-flex w-full items-center justify-center gap-x-2 rounded-md bg-white px-8 py-3 text-base font-semibold text-black shadow-sm sm:w-auto"
				>
					Request a Demo
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="2.5"
						stroke="currentColor"
						class="h-4 w-4 transition-transform group-hover:translate-x-1"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3"
						></path>
					</svg>
				</a>
			</div>
		</div>
		<div class="mt-16 sm:mt-24">
			<div class="mx-auto max-w-5xl">
				<div class="relative aspect-video w-full overflow-hidden rounded-lg border border-white/10">
					<iframe
						class="absolute left-0 top-0 h-full w-full"
						src="https://player.vimeo.com/video/1046099319?app_id=122963&dntp=1&background=1"
						title="Squint Demo Video"
						allow="autoplay; fullscreen; picture-in-picture"
						allowfullscreen
					></iframe>
				</div>
			</div>
		</div>
	</div>
</section>