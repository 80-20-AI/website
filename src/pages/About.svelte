<script>
  import PrivacyDiagram from '../lib/components/PrivacyDiagram.svelte';
  import Button from '../lib/components/Button.svelte';
</script>

<section class="bg-gradient-to-b from-primary-50 to-white py-16 md:py-24">
  <div class="container">
    <div class="max-w-3xl mx-auto text-center mb-16">
      <h1 class="text-3xl md:text-4xl font-semibold text-secondary-900 mb-4">
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
      
      <!-- Our Story -->
      <div class="bg-white rounded-xl shadow-soft overflow-hidden mb-20">
        <div class="p-8 md:p-12">
          <h2 class="text-2xl md:text-3xl font-semibold text-secondary-800 mb-6">
            Our Story
          </h2>
          <div class="space-y-4 text-secondary-700">
            <p>
              80/20 AI was founded in 2024 by a team of AI safety researchers, cybersecurity professionals, and compliance experts who recognized a critical gap in the market: while AI capabilities were advancing rapidly, tools to help organizations manage AI risks were lagging behind.
            </p>
            <p>
              Our founding team witnessed firsthand how organizations struggled to keep up with evolving AI regulations and best practices, often resorting to expensive consultants or taking on significant compliance risks.
            </p>
            <p>
              We built 80/20 AI on the principle that expert AI risk guidance should be accessible to everyone—not just tech giants with large compliance teams. Our name reflects the Pareto principle: we help you achieve 80% of the risk management outcomes with 20% of the traditional effort and cost.
            </p>
            <p>
              Today, we're proud to support organizations across industries in implementing responsible AI practices that protect their users, their reputation, and their bottom line.
            </p>
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
      
      <!-- Team -->
      <div class="mb-20">
        <h2 class="text-2xl md:text-3xl font-semibold text-secondary-800 text-center mb-12">
          Our Leadership Team
        </h2>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div class="bg-white rounded-xl shadow-soft overflow-hidden">
            <img 
              src="https://images.pexels.com/photos/5669619/pexels-photo-5669619.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" 
              alt="Dr. Sarah Chen" 
              class="w-full h-60 object-cover"
            />
            <div class="p-6">
              <h3 class="text-xl font-semibold text-secondary-800 mb-1">Dr. Sarah Chen</h3>
              <p class="text-secondary-600 mb-4">CEO & Co-Founder</p>
              <p class="text-secondary-700 text-sm">
                Former AI ethics researcher with 15+ years in cybersecurity and compliance. Ph.D. in Computer Science from MIT.
              </p>
            </div>
          </div>
          
          <div class="bg-white rounded-xl shadow-soft overflow-hidden">
            <img 
              src="https://images.pexels.com/photos/2379004/pexels-photo-2379004.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" 
              alt="Mark Johnson" 
              class="w-full h-60 object-cover"
            />
            <div class="p-6">
              <h3 class="text-xl font-semibold text-secondary-800 mb-1">Mark Johnson</h3>
              <p class="text-secondary-600 mb-4">CTO & Co-Founder</p>
              <p class="text-secondary-700 text-sm">
                Previously led AI security teams at major tech companies. Pioneered privacy-preserving machine learning techniques.
              </p>
            </div>
          </div>
          
          <div class="bg-white rounded-xl shadow-soft overflow-hidden">
            <img 
              src="https://images.pexels.com/photos/3184405/pexels-photo-3184405.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" 
              alt="Lisa Wong" 
              class="w-full h-60 object-cover"
            />
            <div class="p-6">
              <h3 class="text-xl font-semibold text-secondary-800 mb-1">Lisa Wong</h3>
              <p class="text-secondary-600 mb-4">Chief Risk Officer</p>
              <p class="text-secondary-700 text-sm">
                Former regulatory advisor with expertise in global compliance frameworks and AI governance models.
              </p>
            </div>
          </div>
        </div>
      </div>
      
      <!-- CTA -->
      <div class="bg-gradient-to-br from-primary-600 to-primary-800 rounded-xl shadow-soft overflow-hidden">
        <div class="p-8 md:p-12 text-center">
          <h2 class="text-2xl md:text-3xl font-semibold text-white mb-4">
            Join us in building a safer AI future
          </h2>
          <p class="text-xl text-primary-100 mb-8 max-w-2xl mx-auto">
            Experience how 80/20 AI can transform your approach to AI risk management
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center">
            <Button href="/chat" variant="accent" size="lg">Try the AI Assistant</Button>
            <Button href="/contact" variant="outline" size="lg">Contact Our Team</Button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>