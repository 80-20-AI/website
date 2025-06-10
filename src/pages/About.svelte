<script>
  import PrivacyDiagram from '../lib/components/PrivacyDiagram.svelte';
  import Button from '../lib/components/Button.svelte';
</script>

<section class="bg-gradient-to-b from-primary-50 to-white py-16 md:py-24">
  <div class="container">
    <div class="max-w-3xl mx-auto text-center mb-16">
      <h1 class="text-3xl md:text-4xl font-semibold text-secondary-800 mb-4">
        About 80/20 AI
      </h1>
      <p class="text-xl text-secondary-700">
        We're building a safer future for AI by making expert risk management accessible to everyone
      </p>
    </div>
    
    <!-- Our Mission Section -->
    <div class="max-w-6xl mx-auto mb-20">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div>
          <h2 class="text-3xl md:text-4xl font-semibold text-secondary-800 mb-6">
            Our Mission
          </h2>
          <p class="text-lg text-secondary-700 mb-6 leading-relaxed">
            We believe that organizations shouldn't have to choose between innovation and compliance. Our mission is to make AI risk management accessible, straightforward, and effective.
          </p>
          <p class="text-lg text-secondary-700 mb-8 leading-relaxed">
            The 80/20 Rule AI platform helps you identify and address the 20% of AI risks that cause 80% of potential harm, so you can focus your resources where they matter most.
          </p>
          
          <div class="space-y-6">
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-primary-100 flex items-center justify-center mt-1">
                <svg class="w-5 h-5 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-secondary-800 mb-2">Simplify Compliance</h3>
                <p class="text-secondary-600">We translate complex regulations into actionable steps.</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-primary-100 flex items-center justify-center mt-1">
                <svg class="w-5 h-5 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-secondary-800 mb-2">Protect Your Organization</h3>
                <p class="text-secondary-600">Identify hidden risks in AI tool terms and contracts.</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-primary-100 flex items-center justify-center mt-1">
                <svg class="w-5 h-5 text-primary-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-secondary-800 mb-2">Enable Responsible Innovation</h3>
                <p class="text-secondary-600">Use AI confidently with proper safeguards in place.</p>
              </div>
            </div>
          </div>
        </div>
        
        <div>
          <img 
            src="https://images.pexels.com/photos/3184418/pexels-photo-3184418.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" 
            alt="Team collaborating on AI strategy" 
            class="rounded-xl shadow-soft w-full"
          />
        </div>
      </div>
    </div>
    
    <!-- How We're Different Section -->
    <div class="max-w-6xl mx-auto mb-20">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div class="order-2 lg:order-1">
          <img 
            src="https://images.pexels.com/photos/3183197/pexels-photo-3183197.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" 
            alt="Privacy-first AI development" 
            class="rounded-xl shadow-soft w-full"
          />
        </div>
        
        <div class="order-1 lg:order-2">
          <h2 class="text-3xl md:text-4xl font-semibold text-secondary-800 mb-6">
            How We're Different
          </h2>
          <p class="text-lg text-secondary-700 mb-6 leading-relaxed">
            Unlike traditional consulting firms that charge thousands for basic guidance, we've automated expert knowledge to make it instantly accessible and affordable.
          </p>
          <p class="text-lg text-secondary-700 mb-8 leading-relaxed">
            Our privacy-first approach means your data never trains our models or gets shared with third parties. We're built by cybersecurity professionals who understand that trust is earned through transparency.
          </p>
          
          <div class="space-y-6">
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-accent-100 flex items-center justify-center mt-1">
                <svg class="w-5 h-5 text-accent-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-secondary-800 mb-2">Privacy-First Architecture</h3>
                <p class="text-secondary-600">Your data is never used for training and is automatically deleted after processing.</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-accent-100 flex items-center justify-center mt-1">
                <svg class="w-5 h-5 text-accent-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-secondary-800 mb-2">Instant Expert Guidance</h3>
                <p class="text-secondary-600">Get immediate answers instead of waiting weeks for consultant availability.</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-4">
              <div class="flex-shrink-0 w-8 h-8 rounded-full bg-accent-100 flex items-center justify-center mt-1">
                <svg class="w-5 h-5 text-accent-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-semibold text-secondary-800 mb-2">Affordable Access</h3>
                <p class="text-secondary-600">Get expert-level guidance at a fraction of traditional consulting costs.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
      
    <!-- Why We Built This -->
    <div class="max-w-5xl mx-auto mb-20">
      <div class="bg-white rounded-xl shadow-soft overflow-hidden">
        <div class="p-8 md:p-12">
          <h2 class="text-2xl md:text-3xl font-semibold text-secondary-800 mb-8 text-center">
            Why We Built This
          </h2>
          <div class="space-y-6 text-secondary-700 max-w-4xl mx-auto">
            <p class="text-lg">
              After years of building AI systems for enterprise clients, we saw firsthand how organizations struggled with managing AI risk. The problem wasn't a lack of willingness to comply—it was the overwhelming complexity of regulations and hidden risks in vendor agreements.
            </p>
            <p class="text-lg">
              We realized that our expertise in both AI development and compliance could help bridge this gap. So we built 80/20 Rule AI to automate the risk identification and policy creation processes we had been doing manually for clients.
            </p>
            <div class="text-center py-6">
              <p class="text-xl font-medium text-primary-500 italic">
                We do this for real, and that's why we can automate it.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
      
    <!-- Privacy Architecture -->
    <div class="max-w-5xl mx-auto mb-20">
      <h2 class="text-2xl md:text-3xl font-semibold text-secondary-800 text-center mb-8">
        Our Privacy-First Architecture
      </h2>
      <p class="text-lg text-secondary-700 text-center max-w-3xl mx-auto mb-12">
        We built 80/20 AI with privacy as a core principle. Your data never trains our models and is automatically deleted after processing.
      </p>
      
      <PrivacyDiagram />
    </div>
      
    <!-- From the Founders -->
    <div class="max-w-5xl mx-auto mb-20">
      <div class="bg-white rounded-xl shadow-soft overflow-hidden">
        <div class="p-8 md:p-12">
          <h2 class="text-2xl md:text-3xl font-semibold text-secondary-800 mb-8 text-center">
            From the Founders
          </h2>
          <div class="space-y-6 text-secondary-700 max-w-4xl mx-auto text-lg leading-relaxed">
            <p>
              We created 8020AI for the teams who don't have time to chase every headline. AI is moving fast, and for small, resource-constrained teams, it's tough to know what actually matters or what could quietly introduce risk through contracts, tools, or vendor relationships. We've been in your shoes—responsible for compliance, security, and strategy while juggling limited time and resources.
            </p>
            <p>
              This platform is our answer. 8020AI is built to cut through the noise and help you focus on the things that matter most—without hype, jargon, or guesswork. Our background is in cybersecurity and AI, and everything here is shaped by what we've seen work (and what we've seen go sideways) in the real world.
            </p>
            <p>
              Everything here has been shaped by hands-on experience and a belief that AI should work for people, not the other way around.
            </p>
            <p>
              Thanks for being here. We're excited to build with you.
            </p>
            <div class="text-right mt-8">
              <p class="font-medium text-secondary-800">
                —The Founders<br />
                <span class="text-primary-500">8020AI</span>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
      
    <!-- CTA -->
    <div class="max-w-5xl mx-auto">
      <div class="bg-gradient-to-br from-primary-500 to-primary-600 rounded-xl shadow-soft overflow-hidden">
        <div class="p-8 md:p-12 text-center">
          <h2 class="text-2xl md:text-3xl font-semibold text-white mb-4">
            Join us in building a safer AI future
          </h2>
          <p class="text-xl text-primary-100 mb-8 max-w-2xl mx-auto">
            Experience how 80/20 AI can transform your approach to AI risk management
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center">
            <Button href="/chat" variant="accent" size="lg">Try the AI Assistant</Button>
            <Button href="/contact" variant="secondary" size="lg">Contact Our Team</Button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>