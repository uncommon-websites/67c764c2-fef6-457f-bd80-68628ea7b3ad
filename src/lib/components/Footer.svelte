<footer class="bg-cream-200/50 pt-20 pb-10 border-t border-cream-200">
  <div class="container">
    <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-20">
      <!-- Logo Column -->
      <div class="md:col-span-1">
        <a href="/" class="font-serif text-2xl tracking-wide text-gray-900 block mb-8">MAI</a>
        
        <div class="flex items-center gap-2 mb-4">
           <!-- Toggle Switch Simulation -->
           <button class="bg-white border border-gray-200 rounded-full px-3 py-1 flex items-center gap-2 text-[10px] uppercase tracking-wider font-medium text-gray-500">
             <span>Off</span>
             <span>Accessibility Mode</span>
           </button>
        </div>
      </div>

      <!-- Links Columns -->
      <div class="grid grid-cols-2 md:grid-cols-3 gap-8 md:col-span-3">
        <div class="flex flex-col gap-3">
          {#each ['About', 'News', 'Team', 'Careers'] as item}
            <a href="#" class="text-xs uppercase tracking-widest font-medium text-gray-600 hover:text-gray-900">{item}</a>
          {/each}
        </div>

        <div class="flex flex-col gap-3">
          {#each ['LinkedIn', 'Instagram', 'X'] as item}
            <a href="#" class="text-xs uppercase tracking-widest font-medium text-gray-600 hover:text-gray-900">{item}</a>
          {/each}
        </div>

        <div class="flex flex-col gap-3">
          {#each ['Contact', 'Privacy & Cookies', 'Terms', 'Trademarks', 'Microsoft.com'] as item}
            <a href="#" class="text-xs uppercase tracking-widest font-medium text-gray-600 hover:text-gray-900">{item}</a>
          {/each}
        </div>
      </div>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-4 gap-12 text-[10px] text-gray-500 leading-relaxed border-t border-gray-200/50 pt-8">
      <div class="md:col-start-4">
        <p class="mb-4">© Microsoft 2025</p>
        <p>
          This site runs Microsoft Clarity for behavioral insights. By using this site, you consent to the collection and use of your data, such as how you interact with this website, by Microsoft for product improvements. Learn more <a href="#" class="underline">here</a> and at our <a href="#" class="underline">Privacy Statement</a>.
        </p>
      </div>
    </div>
  </div>
</footer>
