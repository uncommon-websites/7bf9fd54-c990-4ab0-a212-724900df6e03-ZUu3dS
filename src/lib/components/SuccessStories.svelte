<script lang="ts">
  // Types
  type Story = {
    logoSrc: string;
    logoAlt: string;
    text: string;
    href: string;
  };

  // Props
  let { className = '' }: { className?: string } = $props();

  // Data for success stories. Kept inline as per requirements.
  const stories: Story[] = [
    {
      logoSrc: 'https://www.ledr.com/colours/white.jpg',
      logoAlt: 'Acme Manufacturing Logo',
      text: 'How Acme Manufacturing Cut Onboarding Time by 50%',
      href: '#'
    },
    {
      logoSrc: 'https://www.ledr.com/colours/white.jpg',
      logoAlt: 'Apex Industries Logo',
      text: 'Apex Industries Reduces Errors by 30% with Standardized Visual Guides',
      href: '#'
    },
    {
      logoSrc: 'https://www.ledr.com/colours/white.jpg',
      logoAlt: 'Pinnacle Machining Logo',
      text: 'Pinnacle Machining Preserves 20+ Years of Tribal Knowledge',
      href: '#'
    }
  ];
</script>

<section class="py-16 sm:py-24 bg-black font-body {className}">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="mx-auto max-w-4xl text-center">
      <h2 class="text-4xl font-bold tracking-tight sm:text-5xl text-neutral-50 font-display">
        Trusted by Leading Manufacturers
      </h2>
      <p class="mt-6 text-lg leading-8 text-neutral-300">
        Operations managers rely on Squint to standardize work, onboard new hires faster, and capture
        invaluable tribal knowledge.
      </p>
    </div>
    <div class="mt-16">
      <div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
        {#each stories as story}
          <article class="flex flex-col rounded-2xl border border-neutral-800 bg-neutral-900 p-8">
            <img class="h-10 w-auto self-start" src={story.logoSrc} alt={story.logoAlt} />
            <div class="mt-8 flex-grow">
              <p class="text-lg text-neutral-200">{story.text}</p>
            </div>
            <div class="mt-8">
              <a
                href={story.href}
                class="inline-block rounded-lg border border-neutral-700 px-4 py-2 text-sm font-medium text-neutral-50 transition hover:bg-neutral-50 hover:text-neutral-950"
              >
                Read More
              </a>
            </div>
          </article>
        {/each}
      </div>
    </div>
  </div>
</section>