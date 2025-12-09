<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 10;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<nav class="fixed top-0 left-0 w-full z-50 transition-colors duration-200 {isScrolled ? 'bg-[#0b0c0e]/90 backdrop-blur-md border-b border-[#2e3138]' : 'bg-transparent'}">
  <div class="max-w-[1280px] mx-auto px-6 h-16 flex items-center justify-between font-sans text-sm">
    <!-- Left: Logo & Links -->
    <div class="flex items-center gap-8">
      <a href="/" class="text-white font-bold text-2xl tracking-tighter flex items-center gap-2">
        <!-- Logo Icon -->
        <svg viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
          <path d="M3 6h18v2H3V6zm0 5h18v2H3v-2zm0 5h18v2H3v-2z" /> 
        </svg>
        Retool
      </a>

      <div class="hidden lg:flex items-center gap-6 text-sm font-medium text-gray-400">
        <button class="hover:text-white flex items-center gap-1 group transition-colors">
          Platform <span class="group-hover:rotate-180 transition-transform text-[10px] opacity-50">▼</span>
        </button>
        <button class="hover:text-white transition-colors">Solutions</button>
        <button class="hover:text-white transition-colors">Resources</button>
        <button class="hover:text-white transition-colors">Use cases</button>
        <button class="hover:text-white transition-colors">Pricing</button>
      </div>
    </div>

    <!-- Right: Actions -->
    <div class="flex items-center gap-4">
      <button class="text-gray-400 hover:text-white transition-colors">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="11" cy="11" r="8"></circle>
          <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
        </svg>
      </button>
      
      <a href="/login" class="text-gray-300 hover:text-white font-medium text-sm hidden sm:block transition-colors">Sign in</a>
      
      <a href="/demo" class="hidden sm:flex items-center justify-center px-4 py-2 rounded-md border border-gray-600 text-white hover:border-gray-400 transition-colors text-sm font-medium">
        Book a demo
      </a>
      
      <a href="/signup" class="flex items-center justify-center px-4 py-2 rounded-md bg-white text-black hover:bg-gray-200 transition-colors text-sm font-bold">
        Start for free
      </a>
    </div>
  </div>
</nav>
