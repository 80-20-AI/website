<script lang="ts">
  import Pricing from '../../pages/Pricing.svelte';
</script>

<!-- Override the Pricing page header -->
<section class="relative bg-gradient-to-br from-primary-50 via-white to-accent-50 py-16 md:py-24 overflow-hidden">
  <!-- Background decorative elements -->
  <div class="absolute inset-0 overflow-hidden">
    <div class="absolute top-10 left-1/4 w-72 h-72 bg-primary-100/20 rounded-full blur-3xl"></div>
    <div class="absolute bottom-10 right-1/4 w-72 h-72 bg-accent-100/20 rounded-full blur-3xl"></div>
  </div>
  
  <div class="container relative">
    <div class="max-w-4xl mx-auto text-center mb-16">
      <!-- Badge -->
      <div class="inline-flex items-center bg-primary-100/80 backdrop-blur-sm text-primary-700 rounded-full px-4 py-2 text-sm font-medium mb-6">
        <svg class="w-4 h-4 mr-2 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1" />
        </svg>
        Transparent, simple pricing
      </div>
      
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-secondary-800 mb-6 leading-tight">
        Choose Your
        <span class="bg-gradient-to-r from-primary-500 to-accent-500 bg-clip-text text-transparent">
          Plan
        </span>
      </h1>
      
      <p class="text-xl md:text-2xl text-secondary-600 mb-8 max-w-3xl mx-auto leading-relaxed">
        Choose the plan that fits your AI risk management needs. Start free, upgrade when you're ready.
      </p>
      
      <!-- Pricing highlights -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-2xl mx-auto mb-8">
        <div class="flex items-center justify-center space-x-2 text-secondary-600">
          <div class="w-5 h-5 rounded-full bg-primary-100 flex items-center justify-center">
            <svg class="w-3 h-3 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
          </div>
          <span class="text-sm font-medium">No hidden fees</span>
        </div>
        
        <div class="flex items-center justify-center space-x-2 text-secondary-600">
          <div class="w-5 h-5 rounded-full bg-primary-100 flex items-center justify-center">
            <svg class="w-3 h-3 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
          </div>
          <span class="text-sm font-medium">Cancel anytime</span>
        </div>
        
        <div class="flex items-center justify-center space-x-2 text-secondary-600">
          <div class="w-5 h-5 rounded-full bg-primary-100 flex items-center justify-center">
            <svg class="w-3 h-3 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
          </div>
          <span class="text-sm font-medium">14-day free trial</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Use the existing Pricing component but skip its header -->
<div class="pricing-content">
  <Pricing />
</div>

<style>
  /* Hide the original header from the Pricing component */
  :global(.pricing-content section:first-child) {
    padding-top: 0 !important;
  }
  
  :global(.pricing-content h1) {
    display: none;
  }
  
  :global(.pricing-content .max-w-3xl.mx-auto.text-center.mb-16) {
    display: none;
  }
</style>