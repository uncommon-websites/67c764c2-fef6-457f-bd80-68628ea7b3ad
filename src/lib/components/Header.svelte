<script lang="ts">
  let isScrolled = $state(false);

  $effect(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<nav class="fixed top-0 z-50 w-full flex justify-center pt-6 px-4 transition-all duration-300 {isScrolled ? 'pt-2' : 'pt-6'}">
  <div class="w-full max-w-[96%] bg-[#fffaf5] rounded-md shadow-sm h-14 px-6 flex items-center justify-between animate-slide-down delay-0">
      
      <!-- Left: Search -->
      <div class="flex items-center gap-3 w-1/3">
          <button class="text-gray-500 hover:text-gray-800 transition-colors">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-4 h-4">
                  <path stroke-linecap="round" stroke-linejoin="round" d="m21 21-5.197-5.197m0 0A7.5 7.5 0 1 0 5.196 5.196a7.5 7.5 0 0 0 10.607 10.607Z" />
              </svg>
          </button>
          <span class="font-lora text-sm text-[#475569]">Search</span>
      </div>

      <!-- Center: Logo -->
      <div class="w-1/3 flex justify-center">
          <a href="/" class="font-playfair text-lg md:text-2xl tracking-tight text-gray-800 font-semibold whitespace-nowrap">ACS Cloud Partners</a>
      </div>

      <!-- Right: Links -->
      <div class="w-1/3 flex justify-end gap-6 md:gap-8">
          <a href="#network" class="font-lora text-sm text-gray-600 hover:text-gray-900 transition-colors hidden sm:block">Network</a>
          <a href="#solutions" class="font-lora text-sm text-gray-600 hover:text-gray-900 transition-colors hidden sm:block">Solutions</a>
          <a href="#pricing" class="font-lora text-sm text-gray-600 hover:text-gray-900 transition-colors hidden sm:block">Pricing</a>
          <a href="#contact" class="font-lora text-sm text-gray-600 hover:text-gray-900 transition-colors hidden sm:block">Contact</a>
          <!-- Mobile Menu Icon (Hidden on desktop) -->
          <button class="sm:hidden text-gray-600">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
              </svg>
          </button>
      </div>
  </div>
</nav>

<style>
    .font-playfair { font-family: 'Playfair Display', serif; }
    .font-lora { font-family: 'Lora', serif; }
    
    @keyframes slideDown {
        from {
            opacity: 0;
            transform: translateY(-20px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .animate-slide-down {
        opacity: 0;
        animation: slideDown 0.8s cubic-bezier(0.22, 0.61, 0.36, 1) forwards;
    }

    .delay-0 { animation-delay: 0ms; }
</style>
