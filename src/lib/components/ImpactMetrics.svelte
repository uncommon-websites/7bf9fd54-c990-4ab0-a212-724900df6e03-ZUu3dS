<script lang="ts">
  // Props
  let { className = '' }: { className?: string } = $props();
</script>

<!-- 
  Impact Metrics Section
  Highlights key performance indicators and benefits of using Squint.
  This section is designed to be placed on a dark background.
-->
<section class="py-16 sm:py-24 {className}">
  <div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <div class="mx-auto max-w-5xl">
      <div
        class="grid grid-cols-1 divide-y divide-neutral-800 border border-neutral-800 lg:grid-cols-3 lg:divide-x lg:divide-y-0"
      >
        <article class="flex h-full flex-col justify-between p-10">
          <div>
            <div class="flex h-10 w-10 items-center justify-center rounded-lg bg-neutral-900">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="h-6 w-6 text-neutral-400"
                ><path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M12 6v6h4.5m4.5 0a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
                /></svg
              >
            </div>
            <div class="h-3"></div>
            <h4 class="font-display text-xl font-light leading-snug text-white">
              Reduction in Training Time
            </h4>
          </div>
          <div>
            <p class="font-body text-[40px] font-light uppercase leading-tight text-white">
              80% Faster
            </p>
          </div>
        </article>
        <article class="flex h-full flex-col justify-between p-10">
          <div>
            <div class="flex h-10 w-10 items-center justify-center rounded-lg bg-neutral-900">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="h-6 w-6 text-neutral-400"
                ><path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="m16.862 4.487 1.687-1.688a1.875 1.875 0 1 1 2.652 2.652L6.832 19.82a4.5 4.5 0 0 1-1.897 1.13l-2.685.8.8-2.685a4.5 4.5 0 0 1 1.13-1.897L16.863 4.487Zm0 0L19.5 7.125"
                /></svg
              >
            </div>
            <div class="h-3"></div>
            <h4 class="font-display text-xl font-light leading-snug text-white">
              Decrease in Documentation Time
            </h4>
          </div>
          <div>
            <p class="font-body text-[40px] font-light uppercase leading-tight text-white">
              95% Faster
            </p>
          </div>
        </article>
        <article class="flex h-full flex-col p-10">
          <div>
            <h4 class="font-display mb-4 text-xl font-light leading-snug text-white">
              Preserve Critical Tribal Knowledge
            </h4>
            <p class="font-body text-base font-light leading-relaxed text-neutral-300">
              Capture decades of manufacturing expertise from your most experienced workers before they retire, ensuring knowledge continuity across your operations.
            </p>
          </div>
        </article>
      </div>
    </div>
  </div>
</section>