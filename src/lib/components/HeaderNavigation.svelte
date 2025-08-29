<script lang="ts">
  // State for managing mobile menu visibility
  let isMobileMenuOpen = $state(false);

  // Props for allowing external class overrides and additions
  let { className = '' }: { className?: string } = $props();

  // Function to toggle the mobile menu's open/closed state
  function toggleMobileMenu() {
    isMobileMenuOpen = !isMobileMenuOpen;
  }

  // Effect to lock body scroll when the mobile menu is open, preventing
  // the background from scrolling. Includes a cleanup function.
  $effect(() => {
    if (isMobileMenuOpen) {
      const originalOverflow = document.body.style.overflow;
      document.body.style.overflow = 'hidden';
      
      return () => {
        document.body.style.overflow = originalOverflow;
      };
    }
  });
</script>

<header class="fixed top-0 left-0 right-0 z-50 bg-neutral-950/80 backdrop-blur-md {className}">
  <div class="mx-auto flex h-20 max-w-screen-xl items-center justify-between px-4 sm:px-6 lg:px-8">
    <a href="#" class="font-display text-2xl font-bold text-neutral-50">Squint</a>
    
    <!-- Desktop Navigation -->
    <nav class="hidden items-center space-x-8 md:flex">
      <a href="#" class="font-body text-base text-neutral-300 transition-colors hover:text-neutral-50">Product</a>
      <a href="#" class="font-body text-base text-neutral-300 transition-colors hover:text-neutral-50">How It Works</a>
      <a href="#" class="font-body text-base text-neutral-300 transition-colors hover:text-neutral-50">Customers</a>
      <a href="#" class="font-body text-base text-neutral-300 transition-colors hover:text-neutral-50">Security</a>
      <a href="#" class="group inline-flex items-center justify-center whitespace-nowrap rounded-full bg-neutral-50 px-5 py-2.5 font-body text-sm font-semibold text-neutral-950 transition-colors hover:bg-neutral-200">
        Request a Demo
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="ml-1 h-4 w-4 transition-transform group-hover:translate-x-1">
          <path fill-rule="evenodd" d="M2 10a.75.75 0 01.75-.75h12.59l-2.1-1.95a.75.75 0 111.02-1.1l3.5 3.25a.75.75 0 010 1.1l-3.5 3.25a.75.75 0 11-1.02-1.1l2.1-1.95H2.75A.75.75 0 012 10z" clip-rule="evenodd" />
        </svg>
      </a>
    </nav>

    <!-- Mobile Menu Button -->
    <div class="flex items-center md:hidden">
      <button 
        onclick={toggleMobileMenu} 
        class="inline-flex items-center justify-center rounded-md p-2 text-neutral-400 hover:bg-neutral-800 hover:text-neutral-50 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-neutral-50"
        aria-controls="mobile-menu"
        aria-expanded={isMobileMenuOpen}
      >
        <span class="sr-only">Open main menu</span>
        {#if !isMobileMenuOpen}
          <!-- Hamburger icon -->
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
          </svg>
        {:else}
          <!-- Close icon -->
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        {/if}
      </button>
    </div>
  </div>

  <!-- Mobile Menu Panel -->
  {#if isMobileMenuOpen}
    <div class="md:hidden" id="mobile-menu">
      <div class="space-y-1 px-2 pt-2 pb-3 sm:px-3">
        <a href="#" class="block rounded-md px-3 py-2 font-body text-base font-medium text-neutral-300 hover:bg-neutral-800 hover:text-neutral-50">Product</a>
        <a href="#" class="block rounded-md px-3 py-2 font-body text-base font-medium text-neutral-300 hover:bg-neutral-800 hover:text-neutral-50">How It Works</a>
        <a href="#" class="block rounded-md px-3 py-2 font-body text-base font-medium text-neutral-300 hover:bg-neutral-800 hover:text-neutral-50">Customers</a>
        <a href="#" class="block rounded-md px-3 py-2 font-body text-base font-medium text-neutral-300 hover:bg-neutral-800 hover:text-neutral-50">Security</a>
      </div>
      <div class="border-t border-neutral-800 p-4">
        <a href="#" class="group flex w-full items-center justify-center whitespace-nowrap rounded-full bg-neutral-50 px-5 py-2.5 font-body text-sm font-semibold text-neutral-950 transition-colors hover:bg-neutral-200">
          Request a Demo
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="ml-1 h-4 w-4 transition-transform group-hover:translate-x-1">
            <path fill-rule="evenodd" d="M2 10a.75.75 0 01.75-.75h12.59l-2.1-1.95a.75.75 0 111.02-1.1l3.5 3.25a.75.75 0 010 1.1l-3.5 3.25a.75.75 0 11-1.02-1.1l2.1-1.95H2.75A.75.75 0 012 10z" clip-rule="evenodd" />
          </svg>
        </a>
      </div>
    </div>
  {/if}
</header>