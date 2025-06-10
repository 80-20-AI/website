<script lang="ts">
  import Insights from '../../pages/Insights.svelte';
</script>

<!-- Override the Insights page header -->
<section class="relative bg-gradient-to-br from-secondary-50 via-white to-primary-50 py-16 md:py-24 overflow-hidden">
  <!-- Background decorative elements -->
  <div class="absolute inset-0 overflow-hidden">
    <div class="absolute top-20 right-20 w-64 h-64 bg-secondary-100/20 rounded-full blur-3xl"></div>
    <div class="absolute bottom-20 left-20 w-64 h-64 bg-primary-100/20 rounded-full blur-3xl"></div>
  </div>
  
  <div class="container relative">
    <div class="max-w-4xl mx-auto text-center mb-12">
      <!-- Badge -->
      <div class="inline-flex items-center bg-secondary-100/80 backdrop-blur-sm text-secondary-700 rounded-full px-4 py-2 text-sm font-medium mb-6">
        <svg class="w-4 h-4 mr-2 text-secondary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
        </svg>
        Expert analysis & guidance
      </div>
      
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-secondary-800 mb-6 leading-tight">
        AI Risk
        <span class="bg-gradient-to-r from-secondary-600 to-primary-500 bg-clip-text text-transparent">
          Insights
        </span>
      </h1>
      
      <p class="text-xl md:text-2xl text-secondary-600 mb-8 max-w-3xl mx-auto leading-relaxed">
        Expert analysis and guidance on AI risk management, compliance, and governance. Stay ahead of the curve with actionable insights.
      </p>
      
      <!-- Content highlights -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-2xl mx-auto mb-8">
        <div class="text-center">
          <div class="text-2xl font-bold text-secondary-600 mb-1">Weekly</div>
          <div class="text-sm text-secondary-500">Updates</div>
        </div>
        <div class="text-center">
          <div class="text-2xl font-bold text-secondary-600 mb-1">Expert</div>
          <div class="text-sm text-secondary-500">Analysis</div>
        </div>
        <div class="text-center">
          <div class="text-2xl font-bold text-secondary-600 mb-1">Actionable</div>
          <div class="text-sm text-secondary-500">Guidance</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Use the existing Insights component but skip its header -->
<div class="insights-content">
  <Insights />
</div>

<style>
  /* Hide the original header from the Insights component */
  :global(.insights-content section:first-child) {
    padding-top: 0 !important;
  }
  
  :global(.insights-content h1) {
    display: none;
  }
  
  :global(.insights-content .max-w-3xl.mx-auto.text-center.mb-12) {
    display: none;
  }
</style>