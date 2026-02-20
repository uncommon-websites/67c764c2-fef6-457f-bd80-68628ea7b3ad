<script lang="ts">
  const newsItems = [
    {
      title: "The State of Dealership Technology 2025: Integration vs. Fragmentation",
      category: "research",
      readTime: "12 min read",
      type: "strips",
      images: [
        '/generated/image-a-futuristic-car-dashboard-with-advanced-1771551175143-0.webp',
        '/generated/image-a-business-meeting-between-automotive-ex-1771551177372-1.webp',
        '/generated/image-a-digital-map-showing-a-network-of-conne-1771551179424-2.webp'
      ]
    },
    {
      title: "How White-Glove Implementation is Saving GMs 20+ Hours Weekly",
      category: "case study",
      readTime: "8 min read",
      image: "/generated/image-a-business-meeting-between-automotive-ex-1771551177372-1.webp",
      type: "standard"
    },
    {
      title: "ACS Automotive Expands Vetted Provider Network to Include Elite AI Tools",
      category: "announcement",
      readTime: "5 min read",
      image: "/generated/image-a-futuristic-car-dashboard-with-advanced-1771551175143-0.webp",
      type: "standard",
      hasArrow: true
    },
    {
      title: "Guaranteed Lowest Pricing: Why the $150B Market is Ripe for Disruption",
      category: "perspective",
      readTime: "10 min read",
      type: "grid"
    }
  ];
</script>

<section id="news" class="py-32 bg-white">
  <div class="container">
    <div class="text-center mb-24">
      <h2 class="font-playfair text-5xl md:text-6xl text-gray-900 mb-4">Latest <span class="italic text-primary-600">Insights</span></h2>
      <p class="font-lora italic text-2xl md:text-3xl text-gray-500 font-light">Navigating the future of automotive retail.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-x-16 gap-y-24 max-w-6xl mx-auto">
      <!-- Item 1: Vertical Strips -->
      <div class="group cursor-pointer">
        <div class="aspect-square mb-8 flex gap-1 overflow-hidden rounded-lg">
           {#each newsItems[0].images as img}
             <div class="flex-1 bg-cover bg-center transition-transform duration-700 hover:scale-105" style="background-image: url('{img}');"></div>
           {/each}
        </div>
        <h3 class="font-playfair text-3xl leading-tight mb-6 max-w-md">{newsItems[0].title}</h3>
        <div class="flex justify-between items-center text-[10px] uppercase tracking-widest text-gray-500 font-mono border-t border-gray-100 pt-4">
          <span class="bg-primary-50 text-primary-700 px-2 py-1 rounded">{newsItems[0].category}</span>
          <span>{newsItems[0].readTime}</span>
        </div>
      </div>

      <!-- Item 2: Standard Image -->
      <div class="group cursor-pointer md:mt-24">
        <div class="aspect-square overflow-hidden mb-8 w-4/5 mx-auto bg-[#fffaf5] p-4 shadow-sm rotate-1 rounded-lg">
           <img src={newsItems[1].image} alt={newsItems[1].title} class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700 rounded" />
        </div>
        <h3 class="font-playfair text-3xl leading-tight mb-6 max-w-sm mx-auto">{newsItems[1].title}</h3>
        <div class="flex justify-between items-center text-[10px] uppercase tracking-widest text-gray-500 font-mono border-t border-gray-100 pt-4 max-w-sm mx-auto">
          <span class="bg-gray-100 px-2 py-1 rounded">{newsItems[1].category}</span>
          <span>{newsItems[1].readTime}</span>
        </div>
      </div>

      <!-- Item 3: Standard Image -->
      <div class="group cursor-pointer">
        <div class="aspect-square overflow-hidden mb-8 w-4/5 mx-auto shadow-md rounded-lg">
           <img src={newsItems[2].image} alt={newsItems[2].title} class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700" />
        </div>
        <h3 class="font-playfair text-3xl leading-tight mb-6 max-w-sm mx-auto">{newsItems[2].title}</h3>
        <div class="flex justify-between items-center text-[10px] uppercase tracking-widest text-gray-500 font-mono border-t border-gray-100 pt-4 max-w-sm mx-auto">
          <span class="bg-gray-100 px-2 py-1 rounded">{newsItems[2].category}</span>
          {#if newsItems[2].hasArrow}
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="ml-auto text-primary-600"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
          {/if}
        </div>
      </div>

       <!-- Item 4: Grid -->
      <div class="group cursor-pointer md:mt-[-80px]">
        <div class="aspect-square bg-gray-50 p-6 mb-8 relative overflow-hidden rounded-lg">
           <div class="grid grid-cols-2 gap-4 h-full">
             <div class="bg-white p-1 shadow-sm transform -rotate-2 hover:rotate-0 transition-transform duration-500 rounded"><img src="/generated/image-a-digital-map-showing-a-network-of-conne-1771551179424-2.webp" class="w-full h-full object-cover rounded-sm" /></div>
             <div class="bg-white p-1 shadow-sm mt-8 transform rotate-3 hover:rotate-0 transition-transform duration-500 rounded"><img src="/generated/image-a-futuristic-car-dashboard-with-advanced-1771551175143-0.webp" class="w-full h-full object-cover rounded-sm" /></div>
             <div class="bg-white p-1 shadow-sm -mt-8 transform rotate-1 hover:rotate-0 transition-transform duration-500 rounded"><img src="/generated/image-a-business-meeting-between-automotive-ex-1771551177372-1.webp" class="w-full h-full object-cover rounded-sm" /></div>
             <div class="bg-white p-1 shadow-sm transform -rotate-3 hover:rotate-0 transition-transform duration-500 rounded"><img src="/generated/image-a-digital-map-showing-a-network-of-conne-1771551179424-2.webp" class="w-full h-full object-cover rounded-sm" /></div>
           </div>
        </div>
        <h3 class="font-playfair text-3xl leading-tight mb-6">{newsItems[3].title}</h3>
        <div class="flex justify-between items-center text-[10px] uppercase tracking-widest text-gray-500 font-mono border-t border-gray-100 pt-4">
          <span class="bg-gray-100 px-2 py-1 rounded">{newsItems[3].category}</span>
          <span>{newsItems[3].readTime}</span>
        </div>
      </div>
    </div>

    <div class="flex justify-center mt-24">
      <a href="/news" class="inline-flex items-center gap-2 px-8 py-4 bg-primary-600 hover:bg-primary-700 transition-colors rounded-full text-[10px] uppercase tracking-widest font-mono text-white shadow-lg">
        Explore all news
        <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"></line><polyline points="12 5 19 12 12 19"></polyline></svg>
      </a>
    </div>
  </div>
</section>

<style>
  .font-playfair { font-family: 'Playfair Display', serif; }
  .font-lora { font-family: 'Lora', serif; }
  .font-mono { font-family: 'DM Mono', monospace; }
  .text-primary-600 { color: #3d4e68; }
  .text-primary-700 { color: #2f3d51; }
  .bg-primary-50 { background-color: #f0f2f5; }
  .bg-primary-600 { background-color: #3d4e68; }
  .bg-primary-700 { background-color: #2f3d51; }
</style>
