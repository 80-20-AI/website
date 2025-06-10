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
    
    <!-- Mission & Vision -->
    <div class="max-w-5xl mx-auto">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center mb-20">
        <div>
          <h2 class="text-2xl md:text-3xl font-semibold text-secondary-800 mb-6">
            Our Mission
          </h2>
          <p class="text-lg text-secondary-700 mb-4">
            To democratize AI risk management by providing accessible, expert guidance that empowers organizations of all sizes to implement AI responsibly.
          </p>
          <p class="text-lg text-secondary-700">
            We believe that innovation and safety can co-exist when organizations have the right tools to navigate the complex AI risk landscape.
          </p>
        </div>
        <div>
          <img 
            src="https://images.pexels.com/photos/3183197/pexels-photo-3183197.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" 
            alt="80/20 AI Team Collaboration" 
            class="rounded-xl shadow-soft w-full"
          />
        </div>
      </div>
      
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center mb-20">
        <div class="order-2 lg:order-1">
          <img 
            src="https://images.pexels.com/photos/3184418/pexels-photo-3184418.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" 
            alt="80/20 AI Vision" 
            class="rounded-xl shadow-soft w-full"
          />
        </div>
        <div class="order-1 lg:order-2">
          <h2 class="text-2xl md:text-3xl font-semibold text-secondary-800 mb-6">
            Our Vision
          </h2>
          <p class="text-lg text-secondary-700 mb-4">
            We envision a world where AI is ubiquitous yet safe — where every organization deploying AI has the necessary expertise to manage risks effectively.
          </p>
          <p class="text-lg text-secondary-700">
            By combining expert guidance with privacy-first technology, we're creating a future where AI's benefits can be realized while its risks are properly managed.
          </p>
        </div>
      </div>
      
      <!-- Why We Built This -->
      <div class="bg-white rounded-xl shadow-soft overflow-hidden mb-20">
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
      
      <!-- Privacy Architecture -->
      <div class="mb-20">
        <h2 class="text-2xl md:text-3xl font-semibold text-secondary-800 text-center mb-8">
          Our Privacy-First Architecture
        </h2>
        <p class="text-lg text-secondary-700 text-center max-w-3xl mx-auto mb-12">
          We built 80/20 AI with privacy as a core principle. Your data never trains our models and is automatically deleted after processing.
        </p>
        
        <PrivacyDiagram />
      </div>
      
      <!-- From the Founders -->
      <div class="bg-white rounded-xl shadow-soft overflow-hidden mb-20">
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
      
      <!-- CTA -->
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