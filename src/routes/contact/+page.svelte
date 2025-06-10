<script lang="ts">
  import Button from '$lib/components/Button.svelte';
  
  let formData = {
    name: '',
    email: '',
    company: '',
    subject: '',
    message: ''
  };
  
  let sending = false;
  let success = false;
  let error = '';
  
  async function handleSubmit() {
    sending = true;
    error = '';
    
    try {
      // In a real app, this would send to your API
      await new Promise(resolve => setTimeout(resolve, 1000));
      success = true;
      formData = {
        name: '',
        email: '',
        company: '',
        subject: '',
        message: ''
      };
    } catch (err) {
      error = 'Failed to send message. Please try again.';
    } finally {
      sending = false;
    }
  }
</script>

<section class="relative bg-gradient-to-br from-primary-50 via-white to-accent-50 py-16 md:py-24 overflow-hidden">
  <!-- Background decorative elements -->
  <div class="absolute inset-0 overflow-hidden">
    <div class="absolute top-20 left-20 w-64 h-64 bg-primary-100/20 rounded-full blur-3xl"></div>
    <div class="absolute bottom-20 right-20 w-64 h-64 bg-accent-100/20 rounded-full blur-3xl"></div>
  </div>
  
  <div class="container relative">
    <div class="max-w-4xl mx-auto text-center mb-12">
      <!-- Badge -->
      <div class="inline-flex items-center bg-primary-100/80 backdrop-blur-sm text-primary-700 rounded-full px-4 py-2 text-sm font-medium mb-6">
        <svg class="w-4 h-4 mr-2 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
        </svg>
        We're here to help
      </div>
      
      <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-secondary-800 mb-6 leading-tight">
        Get in
        <span class="bg-gradient-to-r from-primary-500 to-accent-500 bg-clip-text text-transparent">
          Touch
        </span>
      </h1>
      
      <p class="text-xl md:text-2xl text-secondary-600 mb-8 max-w-3xl mx-auto leading-relaxed">
        Get in touch with our team for any questions about AI risk management. We're here to help you navigate the complex world of AI compliance.
      </p>
      
      <!-- Response time info -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-lg mx-auto mb-8">
        <div class="text-center">
          <div class="text-2xl font-bold text-primary-500 mb-1">24hrs</div>
          <div class="text-sm text-secondary-600">Response time</div>
        </div>
        <div class="text-center">
          <div class="text-2xl font-bold text-primary-500 mb-1">Expert</div>
          <div class="text-sm text-secondary-600">Support team</div>
        </div>
      </div>
    </div>
    
    <div class="max-w-2xl mx-auto">
      <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-8 border border-white/20">
        {#if success}
          <div class="text-center py-8">
            <div class="w-16 h-16 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mx-auto mb-4">
              <svg class="w-8 h-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
            </div>
            <h2 class="text-2xl font-semibold text-secondary-800 mb-2">Message Sent!</h2>
            <p class="text-secondary-600 mb-6">
              Thank you for reaching out. We'll get back to you within 24 hours.
            </p>
            <Button 
              on:click={() => success = false}
              variant="secondary"
            >
              Send Another Message
            </Button>
          </div>
        {:else}
          <form on:submit|preventDefault={handleSubmit} class="space-y-6">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <label for="name" class="block text-sm font-medium text-secondary-700 mb-1">
                  Name
                </label>
                <input
                  type="text"
                  id="name"
                  bind:value={formData.name}
                  required
                  class="w-full bg-white/70 backdrop-blur-sm rounded-xl border border-white/20 px-4 py-2.5 focus:outline-none focus:ring-2 focus:ring-primary-500 focus:border-primary-500 transition-all duration-200"
                  placeholder="Your name"
                />
              </div>
              
              <div>
                <label for="email" class="block text-sm font-medium text-secondary-700 mb-1">
                  Email
                </label>
                <input
                  type="email"
                  id="email"
                  bind:value={formData.email}
                  required
                  class="w-full bg-white/70 backdrop-blur-sm rounded-xl border border-white/20 px-4 py-2.5 focus:outline-none focus:ring-2 focus:ring-primary-500 focus:border-primary-500 transition-all duration-200"
                  placeholder="you@company.com"
                />
              </div>
            </div>
            
            <div>
              <label for="company" class="block text-sm font-medium text-secondary-700 mb-1">
                Company
              </label>
              <input
                type="text"
                id="company"
                bind:value={formData.company}
                class="w-full bg-white/70 backdrop-blur-sm rounded-xl border border-white/20 px-4 py-2.5 focus:outline-none focus:ring-2 focus:ring-primary-500 focus:border-primary-500 transition-all duration-200"
                placeholder="Your company name"
              />
            </div>
            
            <div>
              <label for="subject" class="block text-sm font-medium text-secondary-700 mb-1">
                Subject
              </label>
              <input
                type="text"
                id="subject"
                bind:value={formData.subject}
                required
                class="w-full bg-white/70 backdrop-blur-sm rounded-xl border border-white/20 px-4 py-2.5 focus:outline-none focus:ring-2 focus:ring-primary-500 focus:border-primary-500 transition-all duration-200"
                placeholder="How can we help?"
              />
            </div>
            
            <div>
              <label for="message" class="block text-sm font-medium text-secondary-700 mb-1">
                Message
              </label>
              <textarea
                id="message"
                bind:value={formData.message}
                required
                rows="5"
                class="w-full bg-white/70 backdrop-blur-sm rounded-xl border border-white/20 px-4 py-2.5 focus:outline-none focus:ring-2 focus:ring-primary-500 focus:border-primary-500 transition-all duration-200"
                placeholder="Tell us about your AI risk management needs..."
              ></textarea>
            </div>
            
            {#if error}
              <div class="bg-red-50 text-red-700 rounded-lg p-4">
                {error}
              </div>
            {/if}
            
            <div class="flex justify-end">
              <Button 
                type="submit" 
                variant="primary"
                disabled={sending}
              >
                {sending ? 'Sending...' : 'Send Message'}
              </Button>
            </div>
          </form>
        {/if}
      </div>
      
      <!-- Alternative Contact Methods -->
      <div class="mt-12 grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 text-center border border-white/20">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mx-auto mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Email</h3>
          <p class="text-secondary-600">
            <a href="mailto:info@8020ruleai.io" class="hover:text-primary-600 transition-colors">
              info@8020ruleai.io
            </a>
          </p>
        </div>
        
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 text-center border border-white/20">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mx-auto mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Support Hours</h3>
          <p class="text-secondary-600">
            Monday - Friday<br />
            9:00 AM - 6:00 PM EST
          </p>
        </div>
        
        <div class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 text-center border border-white/20">
          <div class="w-12 h-12 bg-primary-100 text-primary-600 rounded-full flex items-center justify-center mx-auto mb-4">
            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8h2a2 2 0 012 2v6a2 2 0 01-2 2h-2v4l-4-4H9a1.994 1.994 0 01-1.414-.586m0 0L11 14h4a2 2 0 002-2V6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2v4l.586-.586z" />
            </svg>
          </div>
          <h3 class="text-lg font-semibold text-secondary-800 mb-2">Live Chat</h3>
          <p class="text-secondary-600">
            Available for Pro and<br />
            Enterprise customers
          </p>
        </div>
      </div>
      
      <!-- FAQ Preview -->
      <div class="mt-16">
        <h2 class="text-2xl font-semibold text-secondary-800 text-center mb-8">
          Frequently Asked Questions
        </h2>
        
        <div class="space-y-4">
          <details class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 cursor-pointer group border border-white/20">
            <summary class="font-medium text-secondary-800 flex justify-between items-center">
              How quickly can I expect a response?
              <svg class="w-5 h-5 text-secondary-500 group-open:rotate-180 transition-transform" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </summary>
            <p class="mt-4 text-secondary-600">
              We aim to respond to all inquiries within 24 hours during business days. Pro and Enterprise customers receive priority support with faster response times.
            </p>
          </details>
          
          <details class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 cursor-pointer group border border-white/20">
            <summary class="font-medium text-secondary-800 flex justify-between items-center">
              Can I schedule a demo before purchasing?
              <svg class="w-5 h-5 text-secondary-500 group-open:rotate-180 transition-transform" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </summary>
            <p class="mt-4 text-secondary-600">
              Yes! We offer personalized demos for teams interested in our Pro and Enterprise plans. Use the contact form above to request a demo and we'll set up a time that works for you.
            </p>
          </details>
          
          <details class="bg-white/70 backdrop-blur-sm rounded-xl shadow-soft p-6 cursor-pointer group border border-white/20">
            <summary class="font-medium text-secondary-800 flex justify-between items-center">
              Do you offer custom solutions?
              <svg class="w-5 h-5 text-secondary-500 group-open:rotate-180 transition-transform" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </summary>
            <p class="mt-4 text-secondary-600">
              Yes, our Enterprise plan includes custom solutions tailored to your organization's specific needs. Contact us to discuss your requirements and we'll create a custom package for you.
            </p>
          </details>
        </div>
      </div>
    </div>
  </div>
</section>