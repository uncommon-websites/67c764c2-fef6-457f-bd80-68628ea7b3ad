<script lang="ts">
  let activeTab = 'Copilot';
  const tabs = ['Copilot', 'Bing', 'Edge', 'GroupMe'];
</script>

<section class="py-32 bg-cream-100">
  <div class="container text-center">
    <h2 class="font-serif text-5xl md:text-6xl text-gray-900 mb-8">Core products and<br/>experiences</h2>
    
    <p class="font-serif text-lg text-gray-600 max-w-2xl mx-auto mb-16 leading-relaxed">
      Our major consumer AI products include Copilot, Bing, GroupMe, Edge, and MSN. We also have teams working on Data, Security, Privacy, Monetization, Health, Responsible AI, Commerce, and Microsoft Advertising. Our mission is to build state of the art AI models, and create an AI companion for everyone.
    </p>

    <!-- Tabs -->
    <div class="inline-flex bg-white rounded-full p-1 mb-12 shadow-sm">
      {#each tabs as tab}
        <button 
          class="px-8 py-2 rounded-full text-xs uppercase tracking-widest font-medium transition-all duration-300 {activeTab === tab ? 'bg-white shadow-sm text-gray-900' : 'text-gray-500 hover:text-gray-900'}"
          on:click={() => activeTab = tab}
        >
          {tab}
        </button>
      {/each}
    </div>

    <!-- Product Image -->
    <div class="relative max-w-4xl mx-auto rounded-2xl overflow-hidden shadow-2xl aspect-[16/9] group">
      <img 
        src="https://images.unsplash.com/photo-1664575602554-2087b04935a5?q=80&w=1200&auto=format&fit=crop" 
        alt="Copilot Interface" 
        class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
      />
      
      <!-- Overlay Content (Copilot Logo) -->
      <div class="absolute inset-0 flex flex-col items-center justify-center bg-black/20">
        <h3 class="font-sans font-bold text-5xl md:text-7xl text-white mb-8 tracking-tight drop-shadow-lg">Copilot</h3>
        
        <!-- Search Bar Simulation -->
        <div class="w-full max-w-md bg-white/90 backdrop-blur rounded-full px-4 py-3 flex items-center gap-3 shadow-lg">
          <div class="w-6 h-6 rounded-full bg-gradient-to-tr from-blue-500 to-purple-500"></div>
          <span class="text-gray-500 text-sm">Ask me anything...</span>
          <div class="ml-auto">
             <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-gray-400"><path d="M12 1a3 3 0 0 0-3 3v8a3 3 0 0 0 6 0V4a3 3 0 0 0-3-3z"></path><path d="M19 10v2a7 7 0 0 1-14 0v-2"></path><line x1="12" y1="19" x2="12" y2="23"></line><line x1="8" y1="23" x2="16" y2="23"></line></svg>
          </div>
        </div>
      </div>
    </div>

    <p class="mt-12 text-sm text-gray-600 max-w-lg mx-auto leading-relaxed">
      Copilot is your AI companion that helps you think, create, and get things done, whether you're solving problems, exploring ideas, or just having a great conversation.
    </p>
  </div>
</section>
