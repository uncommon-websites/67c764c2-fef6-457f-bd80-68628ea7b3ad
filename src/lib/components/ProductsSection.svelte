<script lang="ts">
  let activeTab = 'Transformation';
  const tabs = ['Transformation', 'Vetted Network', 'Lowest Pricing', 'White-Glove'];
  
  const content = {
    'Transformation': {
      title: 'Digital Evolution',
      description: 'We modernize your dealership operations with integrated technology systems that eliminate fragmentation and reduce overhead.',
      image: '/generated/image-modern-car-dealership-interior-with-adva-1771551081353-0.webp'
    },
    'Vetted Network': {
      title: 'Elite Providers',
      description: 'Access our exclusive network of vetted technology providers, ensuring you only work with the best in the industry.',
      image: '/generated/image-a-group-of-dealership-managers-looking-a-1771551085978-2.webp'
    },
    'Lowest Pricing': {
      title: 'Guaranteed Savings',
      description: 'We leverage our collective bargaining power to guarantee the lowest pricing on all technology solutions.',
      image: '/generated/image-close-up-of-a-tablet-showing-a-dealershi-1771551083719-1.webp'
    },
    'White-Glove': {
      title: 'Expert Implementation',
      description: 'Our advisors manage the entire implementation process, overcoming integration fears with hands-on support.',
      image: '/generated/image-a-group-of-dealership-managers-looking-a-1771551085978-2.webp'
    }
  };
</script>

<section id="solutions" class="py-32 bg-[#fffaf5]">
  <div class="container text-center">
    <h2 class="font-playfair text-5xl md:text-6xl text-gray-900 mb-8">Comprehensive <span class="italic text-primary-600">Solutions</span></h2>
    
    <p class="font-lora text-lg text-gray-600 max-w-2xl mx-auto mb-16 leading-relaxed">
      ACS Automotive delivers dealership technology transformation via vetted provider networks and guaranteed lowest pricing. We help you navigate the $150B dealer technology market with confidence.
    </p>

    <!-- Tabs -->
    <div class="inline-flex bg-white rounded-full p-1 mb-12 shadow-sm border border-gray-100">
      {#each tabs as tab}
        <button 
          class="px-4 md:px-8 py-2 rounded-full text-[10px] md:text-xs uppercase tracking-widest font-medium transition-all duration-300 {activeTab === tab ? 'bg-primary-600 text-white shadow-md' : 'text-gray-500 hover:text-gray-900'}"
          on:click={() => activeTab = tab}
        >
          {tab}
        </button>
      {/each}
    </div>

    <!-- Product Image -->
    <div class="relative max-w-5xl mx-auto rounded-2xl overflow-hidden shadow-2xl aspect-[16/9] group bg-gray-100">
      {#each tabs as tab}
        {#if activeTab === tab}
          <div class="absolute inset-0 transition-opacity duration-500">
            <img 
              src={content[tab].image} 
              alt={tab} 
              class="w-full h-full object-cover transition-transform duration-1000 group-hover:scale-105"
            />
            
            <!-- Overlay Content -->
            <div class="absolute inset-0 flex flex-col items-center justify-center bg-black/40 text-white p-8">
              <h3 class="font-playfair text-4xl md:text-6xl mb-6 tracking-tight drop-shadow-lg">{content[tab].title}</h3>
              <p class="max-w-xl text-lg md:text-xl font-lora opacity-90 drop-shadow-md">
                {content[tab].description}
              </p>
            </div>
          </div>
        {/if}
      {/each}
    </div>

    <div class="mt-16 grid grid-cols-1 md:grid-cols-3 gap-8">
      <div class="p-8 bg-white rounded-xl shadow-sm border border-gray-100">
        <h4 class="font-playfair text-xl mb-4">Fragmented Vendors</h4>
        <p class="text-sm text-gray-500 font-lora">We consolidate your technology stack, reducing complexity and administrative burden.</p>
      </div>
      <div class="p-8 bg-white rounded-xl shadow-sm border border-gray-100">
        <h4 class="font-playfair text-xl mb-4">High Costs</h4>
        <p class="text-sm text-gray-500 font-lora">Our guaranteed lowest pricing model ensures you never overpay for critical systems.</p>
      </div>
      <div class="p-8 bg-white rounded-xl shadow-sm border border-gray-100">
        <h4 class="font-playfair text-xl mb-4">Integration Fear</h4>
        <p class="text-sm text-gray-500 font-lora">White-glove implementation means we handle the technical hurdles so you don't have to.</p>
      </div>
    </div>
  </div>
</section>

<style>
  .font-playfair { font-family: 'Playfair Display', serif; }
  .font-lora { font-family: 'Lora', serif; }
  .text-primary-600 { color: oklch(0.596 0.145 163.225); }
  .bg-primary-600 { background-color: oklch(0.596 0.145 163.225); }
</style>
