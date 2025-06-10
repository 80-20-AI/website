<script lang="ts">
  import { page } from '$app/stores';
  import { onMount } from 'svelte';
  
  let scrolled = false;
  let menuOpen = false;
  
  function isActive(path: string): boolean {
    return $page.url.pathname === path;
  }
  
  onMount(() => {
    const handleScroll = () => {
      scrolled = window.scrollY > 20;
    };
    
    window.addEventListener('scroll', handleScroll);
    handleScroll(); // Check initial position
    
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });
  
  function toggleMenu() {
    menuOpen = !menuOpen;
  }
  
  function closeMenu() {
    menuOpen = false;
  }
</script>

<header class="{scrolled ? 'bg-white/90 backdrop-blur-md shadow-sm py-3' : 'bg-transparent py-5'} fixed top-0 left-0 right-0 z-50 transition-all duration-300">
  <div class="container flex items-center justify-between">
    <a href="/" class="flex items-center group" on:click={closeMenu}>
      <div class="flex items-center">
        <span class="text-2xl font-display font-black bg-gradient-to-r from-secondary-800 to-secondary-700 bg-clip-text text-transparent">8020 Rule</span>
        <span class="text-2xl font-display font-black text-primary-500 ml-0.5">AI</span>
      </div>
    </a>
    
    <!-- Desktop Navigation -->
    <nav class="hidden md:flex items-center space-x-8">
      <a href="/" class="nav-link {isActive('/') ? 'active' : ''}">Home</a>
      <a href="/chat" class="nav-link {isActive('/chat') ? 'active' : ''}">AI Assistant</a>
      <a href="/policy-builder" class="nav-link {isActive('/policy-builder') ? 'active' : ''}">Policy Builder</a>
      <a href="/consult" class="nav-link {isActive('/consult') ? 'active' : ''}">Consultation</a>
      <a href="/insights" class="nav-link {isActive('/insights') ? 'active' : ''}">Insights</a>
      <a href="/pricing" class="nav-link {isActive('/pricing') ? 'active' : ''}">Pricing</a>
      <a href="/about" class="nav-link {isActive('/about') ? 'active' : ''}">About</a>
    </nav>
    
    <div class="hidden md:flex items-center space-x-3">
      <a 
        href="/login" 
        class="relative inline-flex items-center px-4 py-2.5 text-sm font-medium text-secondary-700 hover:text-secondary-900 transition-all duration-200 group"
      >
        <span class="relative z-10">Log In</span>
        <div class="absolute inset-0 rounded-lg bg-secondary-100/0 group-hover:bg-secondary-100/80 transition-all duration-200"></div>
      </a>
      <a 
        href="/signup" 
        class="relative inline-flex items-center px-5 py-2.5 text-sm font-semibold text-white bg-gradient-to-r from-primary-500 to-primary-600 rounded-lg shadow-sm hover:shadow-md hover:from-primary-600 hover:to-primary-700 transition-all duration-200 group overflow-hidden"
      >
        <span class="relative z-10 flex items-center">
          Sign Up
          <svg class="ml-1.5 w-4 h-4 transition-transform duration-200 group-hover:translate-x-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
          </svg>
        </span>
        <div class="absolute inset-0 bg-gradient-to-r from-white/0 via-white/10 to-white/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-700"></div>
      </a>
    </div>
    
    <!-- Mobile Menu Button -->
    <button class="md:hidden p-2 rounded-lg text-secondary-600 hover:bg-secondary-100/80 transition-colors duration-200" on:click={toggleMenu} aria-label="Menu">
      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 transition-transform duration-200 {menuOpen ? 'rotate-90' : ''}" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d={menuOpen ? "M6 18L18 6M6 6l12 12" : "M4 6h16M4 12h16M4 18h16"} />
      </svg>
    </button>
  </div>
  
  <!-- Mobile Navigation -->
  {#if menuOpen}
    <div class="md:hidden absolute top-full left-0 right-0 bg-white/95 backdrop-blur-md shadow-lg border-t border-secondary-100/50 animate-fade-in">
      <div class="container py-6 flex flex-col space-y-4">
        <a href="/" class="nav-link py-2 {isActive('/') ? 'active' : ''}" on:click={closeMenu}>Home</a>
        <a href="/chat" class="nav-link py-2 {isActive('/chat') ? 'active' : ''}" on:click={closeMenu}>AI Assistant</a>
        <a href="/policy-builder" class="nav-link py-2 {isActive('/policy-builder') ? 'active' : ''}" on:click={closeMenu}>Policy Builder</a>
        <a href="/consult" class="nav-link py-2 {isActive('/consult') ? 'active' : ''}" on:click={closeMenu}>Consultation</a>
        <a href="/insights" class="nav-link py-2 {isActive('/insights') ? 'active' : ''}" on:click={closeMenu}>Insights</a>
        <a href="/pricing" class="nav-link py-2 {isActive('/pricing') ? 'active' : ''}" on:click={closeMenu}>Pricing</a>
        <a href="/about" class="nav-link py-2 {isActive('/about') ? 'active' : ''}" on:click={closeMenu}>About</a>
        
        <div class="pt-4 border-t border-secondary-200/50">
          <div class="flex flex-col space-y-3">
            <a 
              href="/login" 
              class="inline-flex items-center justify-center px-4 py-2.5 text-sm font-medium text-secondary-700 bg-secondary-50 rounded-lg hover:bg-secondary-100 transition-colors duration-200" 
              on:click={closeMenu}
            >
              Log In
            </a>
            <a 
              href="/signup" 
              class="inline-flex items-center justify-center px-4 py-2.5 text-sm font-semibold text-white bg-gradient-to-r from-primary-500 to-primary-600 rounded-lg shadow-sm hover:shadow-md hover:from-primary-600 hover:to-primary-700 transition-all duration-200" 
              on:click={closeMenu}
            >
              <span class="flex items-center">
                Sign Up
                <svg class="ml-1.5 w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                </svg>
              </span>
            </a>
          </div>
        </div>
      </div>
    </div>
  {/if}
</header>

<div class="{scrolled ? 'h-16' : 'h-20'} md:{scrolled ? 'h-16' : 'h-24'} transition-all duration-300"></div>