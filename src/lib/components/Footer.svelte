<footer class="bg-white pt-20 pb-10 border-t border-gray-100">
  <div class="container">
    <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-20">
      <!-- Logo Column -->
      <div class="md:col-span-1">
        <a href="/" class="font-playfair text-2xl tracking-tight text-gray-900 block mb-8 font-semibold">ACS Cloud Partners</a>
        
        <div class="flex items-center gap-2 mb-4">
           <!-- Toggle Switch Simulation -->
           <button class="bg-[#fffaf5] border border-gray-100 rounded-full px-3 py-1 flex items-center gap-2 text-[10px] uppercase tracking-wider font-mono text-gray-500">
             <span>Off</span>
             <span>Accessibility Mode</span>
           </button>
        </div>
      </div>

      <!-- Links Columns -->
      <div class="grid grid-cols-2 md:grid-cols-3 gap-8 md:col-span-3">
        <div class="flex flex-col gap-3">
          {#each ['Network', 'Solutions', 'Team', 'Careers'] as item}
            <a href="#{item.toLowerCase()}" class="text-xs uppercase tracking-widest font-mono text-gray-600 hover:text-primary-600">{item}</a>
          {/each}
        </div>

        <div class="flex flex-col gap-3">
          {#each ['LinkedIn', 'Instagram', 'X'] as item}
            <a href="#" class="text-xs uppercase tracking-widest font-mono text-gray-600 hover:text-primary-600">{item}</a>
          {/each}
        </div>

        <div class="flex flex-col gap-3">
          {#each ['Contact', 'Privacy & Cookies', 'Terms', 'Trademarks'] as item}
            <a href="#" class="text-xs uppercase tracking-widest font-mono text-gray-600 hover:text-primary-600">{item}</a>
          {/each}
        </div>
      </div>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-4 gap-12 text-[10px] text-gray-400 font-mono leading-relaxed border-t border-gray-100 pt-8">
      <div class="md:col-start-4">
        <p class="mb-4">© ACS Cloud Partners 2025</p>
        <p>
          ACS Automotive delivers dealership technology transformation via vetted provider networks and guaranteed lowest pricing.
        </p>
      </div>
    </div>
  </div>
</footer>

<style>
  .font-playfair { font-family: 'Playfair Display', serif; }
  .font-mono { font-family: 'DM Mono', monospace; }
  .text-primary-600 { color: #3d4e68; }
</style>
