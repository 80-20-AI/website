<script lang="ts">
  import Button from '$lib/components/Button.svelte';
</script>

<section class="relative bg-gradient-to-br from-primary-50 via-white to-accent-50 py-16 md:py-24 overflow-hidden">
  <!-- Background decorative elements -->
  <div class="absolute inset-0 overflow-hidden">
    <div class="absolute top-10 left-10 w-72 h-72 bg-primary-100/20 rounded-full blur-3xl"></div>
    <div class="absolute bottom-10 right-10 w-72 h-72 bg-accent-100/20 rounded-full blur-3xl"></div>
  </div>
  
  <div class="container relative">
    <div class="max-w-4xl mx-auto text-center mb-12">
      <!-- Badge -->
      <div class="inline-flex items-center bg-primary-100/80 backdrop-blur-sm text-primary-700 rounded-full px-4 py-2 text-sm font-medium mb-6">
        <svg class="w-4 h-4 mr-2 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z" />
        </svg>
        Expert consultation available
      </div>
      
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-secondary-800 mb-6 leading-tight">
        Expert AI Risk
        <span class="bg-gradient-to-r from-primary-500 to-accent-500 bg-clip-text text-transparent">
          Consultation
        </span>
      </h1>
      
      <p class="text-xl md:text-2xl text-secondary-600 mb-8 max-w-3xl mx-auto leading-relaxed">
        Schedule a one-on-one session with our AI risk specialists for personalized guidance. Get strategic advice tailored to your specific challenges.
      </p>
      
      <!-- Consultation benefits -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-2xl mx-auto mb-8">
        <div class="flex items-center justify-center space-x-3 text-secondary-600">
          <div class="w-6 h-6 rounded-full bg-primary-100 flex items-center justify-center">
            <svg class="w-4 h-4 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
          </div>
          <span class="text-sm font-medium">Personalized guidance</span>
        </div>
        
        <div class="flex items-center justify-center space-x-3 text-secondary-600">
          <div class="w-6 h-6 rounded-full bg-primary-100 flex items-center justify-center">
            <svg class="w-4 h-4 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
          </div>
          <span class="text-sm font-medium">Strategic implementation</span>
        </div>
        
        <div class="flex items-center justify-center space-x-3 text-secondary-600">
          <div class="w-6 h-6 rounded-full bg-primary-100 flex items-center justify-center">
            <svg class="w-4 h-4 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
          </div>
          <span class="text-sm font-medium">Compliance deep-dive</span>
        </div>
        
        <div class="flex items-center justify-center space-x-3 text-secondary-600">
          <div class="w-6 h-6 rounded-full bg-primary-100 flex items-center justify-center">
            <svg class="w-4 h-4 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
            </svg>
          </div>
          <span class="text-sm font-medium">Policy review</span>
        </div>
      </div>
    </div>
    
    <div class="max-w-5xl mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
        <!-- Consultation Info -->
        <div class="lg:col-span-1">
          <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 md:p-8 h-full border border-white/20">
            <h2 class="text-xl font-semibold text-secondary-800 mb-6">
              Why Book a Consultation
            </h2>
            
            <ul class="space-y-4 mb-8">
              <li class="flex items-start">
                <svg class="w-5 h-5 text-accent-500 mt-1 mr-3 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                <span class="text-secondary-700">Personalized guidance for complex AI risk scenarios</span>
              </li>
              <li class="flex items-start">
                <svg class="w-5 h-5 text-accent-500 mt-1 mr-3 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                <span class="text-secondary-700">Strategic advice for AI governance implementation</span>
              </li>
              <li class="flex items-start">
                <svg class="w-5 h-5 text-accent-500 mt-1 mr-3 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                <span class="text-secondary-700">Deep dive into your specific regulatory compliance needs</span>
              </li>
              <li class="flex items-start">
                <svg class="w-5 h-5 text-accent-500 mt-1 mr-3 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                <span class="text-secondary-700">Expert review of your AI policy implementation</span>
              </li>
            </ul>
          </div>
        </div>
        
        <!-- Calendar Embed -->
        <div class="lg:col-span-2">
          <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 md:p-8 border border-white/20">
            <h2 class="text-xl font-semibold text-secondary-800 mb-6">
              Schedule Your Consultation
            </h2>
            
            <!-- Calendar Placeholder -->
            <div class="border border-secondary-200 rounded-lg bg-gradient-to-br from-secondary-50 to-primary-50 p-6 text-center h-96 flex flex-col items-center justify-center">
              <svg class="w-16 h-16 text-secondary-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
              </svg>
              <p class="text-secondary-700 mb-4 font-medium">Select a date and time for your consultation</p>
              <Button variant="primary">View Available Times</Button>
              <p class="text-sm text-secondary-500 mt-4">In a live implementation, a calendar booking system would be embedded here</p>
            </div>
            
            <div class="mt-6">
              <h3 class="font-medium text-secondary-800 mb-3">Consultation Options</h3>
              <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="border border-secondary-200 rounded-lg p-4 bg-white/50">
                  <div class="flex justify-between items-center mb-2">
                    <h4 class="font-medium text-secondary-800">Standard Consultation</h4>
                    <span class="bg-primary-100 text-primary-800 text-xs font-medium px-2.5 py-1 rounded">30 min</span>
                  </div>
                  <p class="text-secondary-600 text-sm mb-3">
                    Quick guidance on specific AI risk questions
                  </p>
                  <div class="flex justify-between items-center">
                    <span class="font-medium text-secondary-800">$149</span>
                    <span class="text-sm text-secondary-500">Free for Pro users</span>
                  </div>
                </div>
                
                <div class="border border-primary-200 bg-primary-50/80 rounded-lg p-4">
                  <div class="flex justify-between items-center mb-2">
                    <h4 class="font-medium text-secondary-800">Deep Dive Session</h4>
                    <span class="bg-primary-100 text-primary-800 text-xs font-medium px-2.5 py-1 rounded">60 min</span>
                  </div>
                  <p class="text-secondary-600 text-sm mb-3">
                    Comprehensive review and strategic planning
                  </p>
                  <div class="flex justify-between items-center">
                    <span class="font-medium text-secondary-800">$299</span>
                    <span class="text-sm text-secondary-500">Free for Enterprise</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Testimonials -->
      <div class="mt-16">
        <h2 class="text-2xl font-semibold text-secondary-800 text-center mb-8">
          What Our Clients Say
        </h2>
        
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 border border-white/20">
            <div class="flex items-center mb-4">
              <div class="w-12 h-12 rounded-full bg-primary-100 flex items-center justify-center mr-4">
                <svg class="w-6 h-6 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                </svg>
              </div>
              <div>
                <p class="font-medium text-secondary-800">Emily Rodriguez</p>
                <p class="text-sm text-secondary-600">CTO, HealthTech Innovations</p>
              </div>
            </div>
            <p class="text-secondary-700 italic">
              "The consultation session provided exactly what we needed to navigate AI compliance in healthcare. The guidance was practical and immediately actionable."
            </p>
          </div>
          
          <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 border border-white/20">
            <div class="flex items-center mb-4">
              <div class="w-12 h-12 rounded-full bg-primary-100 flex items-center justify-center mr-4">
                <svg class="w-6 h-6 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                </svg>
              </div>
              <div>
                <p class="font-medium text-secondary-800">David Kim</p>
                <p class="text-sm text-secondary-600">Legal Director, Finance Solutions</p>
              </div>
            </div>
            <p class="text-secondary-700 italic">
              "Having an expert walk through our specific AI governance challenges saved us months of research and potential compliance issues."
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>