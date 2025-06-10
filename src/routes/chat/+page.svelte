<script lang="ts">
  import ChatBox from '$lib/components/Chat/ChatBox.svelte';
  import Button from '$lib/components/Button.svelte';
</script>

<section class="relative bg-gradient-to-br from-primary-50 via-white to-accent-50 py-16 md:py-24 overflow-hidden">
  <!-- Background decorative elements -->
  <div class="absolute inset-0 overflow-hidden">
    <div class="absolute -top-40 -right-40 w-80 h-80 bg-primary-100/30 rounded-full blur-3xl"></div>
    <div class="absolute -bottom-40 -left-40 w-80 h-80 bg-accent-100/30 rounded-full blur-3xl"></div>
  </div>
  
  <div class="container relative">
    <div class="max-w-4xl mx-auto text-center mb-12">
      <!-- Badge -->
      <div class="inline-flex items-center bg-primary-100/80 backdrop-blur-sm text-primary-700 rounded-full px-4 py-2 text-sm font-medium mb-6">
        <svg class="w-4 h-4 mr-2 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
        </svg>
        AI-powered risk guidance
      </div>
      
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-secondary-800 mb-6 leading-tight">
        Your AI Risk
        <span class="bg-gradient-to-r from-primary-500 to-accent-500 bg-clip-text text-transparent">
          Assistant
        </span>
      </h1>
      
      <p class="text-xl md:text-2xl text-secondary-600 mb-8 max-w-3xl mx-auto leading-relaxed">
        Get expert guidance on AI regulations, compliance requirements, and best practices in real-time. No waiting, no guesswork.
      </p>
      
      <!-- Quick stats -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-2xl mx-auto mb-8">
        <div class="text-center">
          <div class="text-2xl font-bold text-primary-500 mb-1">24/7</div>
          <div class="text-sm text-secondary-600">Available</div>
        </div>
        <div class="text-center">
          <div class="text-2xl font-bold text-primary-500 mb-1">Instant</div>
          <div class="text-sm text-secondary-600">Responses</div>
        </div>
        <div class="text-center">
          <div class="text-2xl font-bold text-primary-500 mb-1">Expert</div>
          <div class="text-sm text-secondary-600">Knowledge</div>
        </div>
      </div>
    </div>
    
    <div class="max-w-4xl mx-auto">
      <ChatBox />
      
      <div class="mt-10 grid md:grid-cols-3 gap-6">
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 border border-white/20 hover:shadow-hover transition-all duration-200">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Ask About Regulations</h3>
          <p class="text-secondary-600 mb-4">
            "What does the EU AI Act require for my generative AI system?"
          </p>
          <Button variant="text" size="sm">Ask this question</Button>
        </div>
        
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 border border-white/20 hover:shadow-hover transition-all duration-200">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Vendor Assessment</h3>
          <p class="text-secondary-600 mb-4">
            "What should I look for when evaluating an AI vendor's compliance?"
          </p>
          <Button variant="text" size="sm">Ask this question</Button>
        </div>
        
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 border border-white/20 hover:shadow-hover transition-all duration-200">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Policy Requirements</h3>
          <p class="text-secondary-600 mb-4">
            "What policies should my organization have for AI governance?"
          </p>
          <Button variant="text" size="sm">Ask this question</Button>
        </div>
      </div>
      
      <div class="mt-12 bg-white/60 backdrop-blur-sm rounded-xl p-6 md:p-8 border border-white/20">
        <div class="flex flex-col md:flex-row items-center">
          <div class="mb-6 md:mb-0 md:mr-8">
            <h3 class="text-xl font-semibold text-secondary-800 mb-2">Need more comprehensive assistance?</h3>
            <p class="text-secondary-600">
              Upgrade to our Pro plan for unlimited access, document analysis, and additional features.
            </p>
          </div>
          <div class="flex-shrink-0">
            <Button href="/pricing" variant="primary">View Pricing Plans</Button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>