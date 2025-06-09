<script>
  import { onMount } from 'svelte';
  import Button from '$lib/components/Button.svelte';
  import HowItWorks from '$lib/components/HowItWorks.svelte';
  import TrustIndicator from '$lib/components/TrustIndicator.svelte';
  
  // Trust indicators data
  const trustIndicators = [
    {
      title: "Privacy-First Architecture",
      description: "Your data never trains our models and is automatically deleted after processing.",
      icon: '<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />'
    },
    {
      title: "Built by Cybersecurity Professionals",
      description: "Our team combines decades of security, compliance, and AI expertise.",
      icon: '<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />'
    },
    {
      title: "Aligned to NIST AI RMF",
      description: "Our approach follows the most trusted AI risk management frameworks in the industry.",
      icon: '<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4" />'
    }
  ];
  
  onMount(() => {
    const elements = document.querySelectorAll('.animate-on-scroll');
    
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.1 });
    
    elements.forEach(element => {
      observer.observe(element);
    });
  });
</script>

<!-- Hero Section -->
<section class="bg-gradient-to-b from-primary-50 to-white pt-16 pb-24 md:pt-24 md:pb-32">
  <div class="container">
    <div class="max-w-3xl mx-auto text-center">
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-secondary-800 mb-6 leading-tight">
        AI moves fast, risk moves faster.
      </h1>
      <p class="text-xl md:text-2xl text-secondary-700 mb-8 md:mb-12">
        Your expert AI risk analyst, built to help you navigate compliance, strategy, and risk without the overhead.
      </p>
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <Button href="/chat" variant="primary" size="lg">Try the AI Risk Assistant – Free</Button>
        <Button href="/consult" variant="secondary" size="lg">Book a Live Consultation</Button>
      </div>
    </div>
  </div>
</section>

<!-- Trust Indicators Section -->
<section class="py-16 md:py-24 bg-white">
  <div class="container">
    <h2 class="text-3xl md:text-4xl font-semibold text-center text-secondary-800 mb-12">
      Trusted AI Risk Guidance
    </h2>
    
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      {#each trustIndicators as indicator, i}
        <div class="animate-on-scroll" style="transition-delay: {i * 100}ms">
          <TrustIndicator 
            title={indicator.title} 
            description={indicator.description} 
            icon={indicator.icon} 
          />
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- How It Works Section -->
<HowItWorks />

<!-- Privacy Architecture Section -->
<section class="bg-gray-50 py-16 md:py-24">
  <div class="container">
    <div class="max-w-6xl mx-auto">
      <div class="text-center mb-12">
        <h2 class="text-3xl md:text-4xl font-semibold text-secondary-800 mb-4">
          Privacy Architecture
        </h2>
        <p class="text-lg text-secondary-600 max-w-2xl mx-auto">
          We've built our platform with privacy as a first principle. Here's how we protect your data.
        </p>
      </div>
      
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <!-- Left side - Privacy features -->
        <div class="space-y-8">
          <div class="bg-white rounded-2xl p-6 shadow-soft">
            <h3 class="text-xl font-semibold text-secondary-800 mb-4">Anonymization Layer</h3>
            <p class="text-secondary-600 mb-6">
              All data that passes through our system is processed through our anonymization layer, which removes identifying information before analysis.
            </p>
            
            <div class="space-y-4">
              <div class="flex items-start space-x-3">
                <div class="flex-shrink-0 w-5 h-5 rounded-full bg-accent-100 flex items-center justify-center mt-0.5">
                  <svg class="w-3 h-3 text-accent-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                </div>
                <div>
                  <h4 class="font-medium text-secondary-800">No Model Training</h4>
                  <p class="text-sm text-secondary-600">We never use your data to train our AI models.</p>
                </div>
              </div>
              
              <div class="flex items-start space-x-3">
                <div class="flex-shrink-0 w-5 h-5 rounded-full bg-accent-100 flex items-center justify-center mt-0.5">
                  <svg class="w-3 h-3 text-accent-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                </div>
                <div>
                  <h4 class="font-medium text-secondary-800">No Data Retention</h4>
                  <p class="text-sm text-secondary-600">Your data is processed and then immediately discarded.</p>
                </div>
              </div>
              
              <div class="flex items-start space-x-3">
                <div class="flex-shrink-0 w-5 h-5 rounded-full bg-accent-100 flex items-center justify-center mt-0.5">
                  <svg class="w-3 h-3 text-accent-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                </div>
                <div>
                  <h4 class="font-medium text-secondary-800">No Vendor Sharing</h4>
                  <p class="text-sm text-secondary-600">We never share your data with third-party vendors.</p>
                </div>
              </div>
              
              <div class="flex items-start space-x-3">
                <div class="flex-shrink-0 w-5 h-5 rounded-full bg-red-100 flex items-center justify-center mt-0.5">
                  <svg class="w-3 h-3 text-red-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                </div>
                <div>
                  <h4 class="font-medium text-secondary-800">No Hidden Terms</h4>
                  <p class="text-sm text-secondary-600">Unlike many AI tools, we're transparent about how we handle your data.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Right side - Visual diagram -->
        <div class="flex justify-center">
          <div class="bg-white rounded-2xl p-8 shadow-soft max-w-md w-full">
            <div class="flex items-center justify-center mb-6">
              <div class="w-16 h-16 bg-primary-100 rounded-full flex items-center justify-center">
                <svg class="w-8 h-8 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
                </svg>
              </div>
            </div>
            
            <!-- Flow diagram -->
            <div class="space-y-4">
              <div class="flex items-center justify-between">
                <div class="bg-gray-100 rounded-lg px-4 py-2 text-sm font-medium text-secondary-700">
                  Your Data
                </div>
                <svg class="w-5 h-5 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                </svg>
                <div class="bg-primary-100 rounded-lg px-4 py-2 text-sm font-medium text-primary-700">
                  Anonymization
                </div>
              </div>
              
              <div class="flex justify-center">
                <svg class="w-5 h-5 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
                </svg>
              </div>
              
              <div class="flex items-center justify-between">
                <div class="bg-accent-100 rounded-lg px-4 py-2 text-sm font-medium text-accent-700">
                  Analysis
                </div>
                <svg class="w-5 h-5 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
                </svg>
                <div class="bg-gray-100 rounded-lg px-4 py-2 text-sm font-medium text-secondary-700">
                  Results
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CTA Section -->
<section class="bg-white py-16 md:py-20">
  <div class="container text-center">
    <h2 class="text-3xl md:text-4xl font-semibold text-secondary-800 mb-6">
      Ready to reduce your AI risk?
    </h2>
    <p class="text-xl text-secondary-600 mb-8 max-w-2xl mx-auto">
      Start with our free AI assistant or book a consultation with our experts to get personalized guidance.
    </p>
    <div class="flex flex-col sm:flex-row gap-4 justify-center">
      <Button href="/chat" variant="primary" size="lg">Try the AI Assistant – Free</Button>
      <Button href="/consult" variant="secondary" size="lg">Book a Live Consultation</Button>
    </div>
  </div>
</section>