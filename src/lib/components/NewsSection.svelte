<script lang="ts">
  const newsItems = [
    {
      title: "It's About Time: The Copilot Usage Report 2025",
      category: "research",
      readTime: "20 min read",
      type: "strips"
    },
    {
      title: "Towards Humanist Superintelligence",
      category: "announcements",
      readTime: "20 min read",
      image: "https://images.unsplash.com/photo-1578301978693-85fa9c0320b9?q=80&w=1000&auto=format&fit=crop",
      type: "standard"
    },
    {
      title: "Copilot Fall Release: A big step forward in making AI more personal, useful, and human-centered",
      category: "copilot",
      readTime: "",
      image: "https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?q=80&w=1000&auto=format&fit=crop",
      type: "standard",
      hasArrow: true
    },
    {
      title: "Introducing MAI-Image-1, debuting in the top 10 on LMArena",
      category: "models",
      readTime: "4 min read",
      type: "grid"
    }
  ];
</script>

<section class="py-32 bg-cream-100">
  <div class="container">
    <div class="text-center mb-24">
      <h2 class="font-serif text-5xl md:text-6xl text-gray-900 mb-4">Latest news</h2>
      <p class="font-serif italic text-4xl md:text-5xl text-gray-600 font-light">Stories. Updates. Perspectives.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-x-16 gap-y-24 max-w-6xl mx-auto">
      <!-- Item 1: Vertical Strips -->
      <div class="group cursor-pointer">
        <div class="aspect-square mb-8 flex gap-1 overflow-hidden">
           <div class="flex-1 bg-cover bg-center transition-transform duration-700 hover:scale-105" style="background-image: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?q=80&w=600&auto=format&fit=crop');"></div>
           <div class="flex-1 bg-cover bg-center transition-transform duration-700 hover:scale-105" style="background-image: url('https://images.unsplash.com/photo-1511884642898-4c92249f20b6?q=80&w=600&auto=format&fit=crop');"></div>
           <div class="flex-1 bg-cover bg-center transition-transform duration-700 hover:scale-105" style="background-image: url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=600&auto=format&fit=crop');"></div>
        </div>
        <h3 class="font-serif text-3xl leading-tight mb-6 max-w-md">{newsItems[0].title}</h3>
        <div class="flex justify-between items-center text-[10px] uppercase tracking-widest text-gray-500 font-medium border-t border-gray-200 pt-4">
          <span class="bg-blue-50 text-blue-800 px-2 py-1 rounded">{newsItems[0].category}</span>
          <span>{newsItems[0].readTime}</span>
        </div>
      </div>

      <!-- Item 2: Standard Image -->
      <div class="group cursor-pointer md:mt-24">
        <div class="aspect-square overflow-hidden mb-8 w-4/5 mx-auto bg-white p-4 shadow-sm rotate-1">
           <img src={newsItems[1].image} alt={newsItems[1].title} class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700" />
        </div>
        <h3 class="font-serif text-3xl leading-tight mb-6 max-w-sm mx-auto">{newsItems[1].title}</h3>
        <div class="flex justify-between items-center text-[10px] uppercase tracking-widest text-gray-500 font-medium border-t border-gray-200 pt-4 max-w-sm mx-auto">
          <span class="bg-gray-100 px-2 py-1 rounded">{newsItems[1].category}</span>
          <span>{newsItems[1].readTime}</span>
        </div>
      </div>

      <!-- Item 3: Standard Image -->
      <div class="group cursor-pointer">
        <div class="aspect-square overflow-hidden mb-8 w-4/5 mx-auto shadow-md">
           <img src={newsItems[2].image} alt={newsItems[2].title} class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700" />
        </div>
        <h3 class="font-serif text-3xl leading-tight mb-6 max-w-sm mx-auto">{newsItems[2].title}</h3>
        <div class="flex justify-between items-center text-[10px] uppercase tracking-widest text-gray-500 font-medium border-t border-gray-200 pt-4 max-w-sm mx-auto">
          <span class="bg-gray-100 px-2 py-1 rounded">{newsItems[2].category}</span>
          {#if newsItems[2].hasArrow}
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="ml-auto"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
          {/if}
        </div>
      </div>

       <!-- Item 4: Grid -->
      <div class="group cursor-pointer md:mt-[-80px]">
        <div class="aspect-square bg-gray-50 p-6 mb-8 relative overflow-hidden">
           <div class="grid grid-cols-2 gap-4 h-full">
             <div class="bg-white p-1 shadow-sm transform -rotate-2 hover:rotate-0 transition-transform duration-500"><img src="https://images.unsplash.com/photo-1501854140884-074bf6b24363?q=80&w=400" class="w-full h-full object-cover" /></div>
             <div class="bg-white p-1 shadow-sm mt-8 transform rotate-3 hover:rotate-0 transition-transform duration-500"><img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?q=80&w=400" class="w-full h-full object-cover" /></div>
             <div class="bg-white p-1 shadow-sm -mt-8 transform rotate-1 hover:rotate-0 transition-transform duration-500"><img src="https://images.unsplash.com/photo-1472214103451-9374bd1c798e?q=80&w=400" class="w-full h-full object-cover" /></div>
             <div class="bg-white p-1 shadow-sm transform -rotate-3 hover:rotate-0 transition-transform duration-500"><img src="https://images.unsplash.com/photo-1426604966848-d7adac402bff?q=80&w=400" class="w-full h-full object-cover" /></div>
           </div>
        </div>
        <h3 class="font-serif text-3xl leading-tight mb-6">{newsItems[3].title}</h3>
        <div class="flex justify-between items-center text-[10px] uppercase tracking-widest text-gray-500 font-medium border-t border-gray-200 pt-4">
          <span class="bg-gray-100 px-2 py-1 rounded">{newsItems[3].category}</span>
          <span>{newsItems[3].readTime}</span>
        </div>
      </div>
    </div>

    <div class="flex justify-center mt-24">
      <a href="/news" class="inline-flex items-center gap-2 px-6 py-3 bg-cream-200 hover:bg-cream-300 transition-colors rounded-full text-[10px] uppercase tracking-widest font-medium text-gray-900">
        All news
        <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"></line><polyline points="12 5 19 12 12 19"></polyline></svg>
      </a>
    </div>
  </div>
</section>
