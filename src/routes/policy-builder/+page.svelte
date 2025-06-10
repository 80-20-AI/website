<script lang="ts">
  import PolicyForm from '$lib/components/PolicyForm.svelte';
</script>

<section class="relative bg-gradient-to-br from-primary-50 via-white to-accent-50 py-16 md:py-24 overflow-hidden">
  <!-- Background decorative elements -->
  <div class="absolute inset-0 overflow-hidden">
    <div class="absolute top-20 right-10 w-64 h-64 bg-primary-100/20 rounded-full blur-3xl"></div>
    <div class="absolute bottom-20 left-10 w-64 h-64 bg-accent-100/20 rounded-full blur-3xl"></div>
    <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-r from-primary-100/10 to-accent-100/10 rounded-full blur-3xl"></div>
  </div>
  
  <div class="container relative">
    <div class="max-w-4xl mx-auto text-center mb-12">
      <!-- Badge -->
      <div class="inline-flex items-center bg-primary-100/80 backdrop-blur-sm text-primary-700 rounded-full px-4 py-2 text-sm font-medium mb-6">
        <svg class="w-4 h-4 mr-2 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
        </svg>
        Automated policy generation
      </div>
      
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-secondary-800 mb-6 leading-tight">
        AI Policy
        <span class="bg-gradient-to-r from-primary-500 to-accent-500 bg-clip-text text-transparent">
          Builder
        </span>
      </h1>
      
      <p class="text-xl md:text-2xl text-secondary-600 mb-8 max-w-3xl mx-auto leading-relaxed">
        Create custom AI governance policies tailored to your organization's specific needs. Professional-grade templates in minutes, not months.
      </p>
      
      <!-- Process steps preview -->
      <div class="grid grid-cols-1 md:grid-cols-4 gap-4 max-w-3xl mx-auto mb-8">
        <div class="flex items-center justify-center space-x-2 text-secondary-600">
          <div class="w-8 h-8 rounded-full bg-primary-100 flex items-center justify-center text-primary-600 font-semibold text-sm">1</div>
          <span class="text-sm font-medium">Organization</span>
        </div>
        <div class="flex items-center justify-center space-x-2 text-secondary-600">
          <div class="w-8 h-8 rounded-full bg-primary-100 flex items-center justify-center text-primary-600 font-semibold text-sm">2</div>
          <span class="text-sm font-medium">AI Usage</span>
        </div>
        <div class="flex items-center justify-center space-x-2 text-secondary-600">
          <div class="w-8 h-8 rounded-full bg-primary-100 flex items-center justify-center text-primary-600 font-semibold text-sm">3</div>
          <span class="text-sm font-medium">Governance</span>
        </div>
        <div class="flex items-center justify-center space-x-2 text-secondary-600">
          <div class="w-8 h-8 rounded-full bg-primary-100 flex items-center justify-center text-primary-600 font-semibold text-sm">4</div>
          <span class="text-sm font-medium">Generate</span>
        </div>
      </div>
    </div>
    
    <div class="max-w-4xl mx-auto">
      <PolicyForm />
      
      <div class="mt-12 grid md:grid-cols-3 gap-6">
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 border border-white/20 hover:shadow-hover transition-all duration-200">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21h10a2 2 0 002-2V9.414a1 1 0 00-.293-.707l-5.414-5.414A1 1 0 0012.586 3H7a2 2 0 00-2 2v14a2 2 0 002 2z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Complete Templates</h3>
          <p class="text-secondary-600">
            Professionally crafted policy templates based on industry standards and best practices
          </p>
        </div>
        
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 border border-white/20 hover:shadow-hover transition-all duration-200">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Fully Customizable</h3>
          <p class="text-secondary-600">
            Tailor policies to your specific industry, region, and unique compliance requirements
          </p>
        </div>
        
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 border border-white/20 hover:shadow-hover transition-all duration-200">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Compliance-Ready</h3>
          <p class="text-secondary-600">
            Aligned with key AI regulations and frameworks like NIST AI RMF and EU AI Act
          </p>
        </div>
      </div>
    </div>
  </div>
</section>