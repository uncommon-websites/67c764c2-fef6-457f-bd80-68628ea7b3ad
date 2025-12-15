<script lang="ts">
  let isScrolled = false;

  function handleScroll() {
    isScrolled = window.scrollY > 10;
  }
</script>

<svelte:window on:scroll={handleScroll} />

<header class="sticky top-0 z-50 w-full bg-cream-100/95 backdrop-blur-sm transition-all duration-300 border-b border-transparent {isScrolled ? 'border-cream-200 shadow-sm' : ''}">
  <div class="container flex h-20 items-center justify-between">
    <!-- Search -->
    <button class="flex items-center gap-3 text-xs uppercase tracking-widest font-medium text-gray-900 hover:opacity-70 transition-opacity">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <circle cx="11" cy="11" r="8"></circle>
        <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
      </svg>
      <span>Search</span>
    </button>

    <!-- Logo -->
    <a href="/" class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 font-serif text-3xl tracking-wide text-gray-900">
      MAI
    </a>

    <!-- Navigation -->
    <nav class="hidden md:flex items-center gap-8">
      {#each ['About', 'News', 'Team', 'Careers'] as item}
        <a href="#{item.toLowerCase()}" class="text-[10px] uppercase tracking-widest font-medium text-gray-900 hover:opacity-70 transition-opacity">
          {item}
        </a>
      {/each}
    </nav>
    
    <!-- Mobile Menu Button (Hidden on desktop) -->
    <button class="md:hidden">
       <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <line x1="3" y1="12" x2="21" y2="12"></line>
        <line x1="3" y1="6" x2="21" y2="6"></line>
        <line x1="3" y1="18" x2="21" y2="18"></line>
      </svg>
    </button>
  </div>
</header>
