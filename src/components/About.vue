<template>
  <section class="space-y-6">
    <div class="flex items-center gap-4 mb-8">
      <h2 class="text-3xl font-bold font-mono text-white">
        <span class="text-iowa-gold">01.</span> About Me
      </h2>
      <div class="h-px bg-gray-700 flex-1"></div>
    </div>
    
    <div class="grid md:grid-cols-3 gap-8">
      <div class="md:col-span-2 space-y-4 text-gray-300 leading-relaxed">
        <p>
          I am a Computer Science & Engineering student at the <span class="text-iowa-gold font-semibold">University of Iowa</span>, 
          passionate about building robust software solutions and exploring the intersections of Artificial Intelligence, 
          data systems, and cloud infrastructure.
        </p>
        <p>
          My journey in tech is driven by a curiosity to understand how complex systems work and a desire to create 
          impactful tools. Whether I am writing scalable backend services, training machine learning models, or crafting 
          intuitive user interfaces, I love the process of turning ideas into reality through code.
        </p>
      </div>
      <div class="flex justify-center items-center">
        <!-- Cute graphic replacing a photo -->
        <div class="w-48 h-48 bg-gray-900 rounded-2xl pixel-corners border border-gray-700 flex items-center justify-center hover-lift relative group">
           <svg class="w-24 h-24 text-iowa-gold" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path></svg>
           <div class="absolute -bottom-3 -right-3 text-3xl opacity-0 group-hover:opacity-100 transition-opacity transform group-hover:scale-110">✨</div>
        </div>
      </div>
    </div>
  </section>
</template>

