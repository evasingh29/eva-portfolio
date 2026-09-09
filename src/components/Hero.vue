<template>
  <section class="flex flex-col-reverse md:flex-row items-center justify-between gap-12 pt-8">
    <div class="flex-1 space-y-6">
      <div>
        <p class="font-mono text-iowa-gold mb-2">Hello! I am</p>
        <h1 class="text-5xl md:text-7xl font-bold text-white mb-4">Eva Singh.</h1>
        <h2 class="text-2xl md:text-3xl text-gray-400">Computer Science & Engineering Student</h2>
      </div>
      
      <p class="text-gray-300 max-w-lg leading-relaxed">
        I build software, work across frontend and backend systems, and have a deep interest in data, AI, and cloud technologies. Currently studying at the University of Iowa.
      </p>

      <div class="flex flex-wrap items-center gap-4 pt-4">
        <a href="/resume.pdf" target="_blank" class="border border-iowa-gold text-iowa-gold px-6 py-2 rounded hover:bg-iowa-gold/10 transition-colors">
          Resume
        </a>
        <a href="https://github.com/evasingh29" target="_blank" class="text-gray-400 hover:text-white p-2 transition-colors" title="GitHub" aria-label="GitHub">
          <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
        </a>
        <a href="https://www.linkedin.com/in/eva-singh295/" target="_blank" class="text-gray-400 hover:text-white p-2 transition-colors" title="LinkedIn" aria-label="LinkedIn">
           <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
        </a>
        <a href="mailto:evasinghwork@gmail.com" class="text-gray-400 hover:text-white p-2 transition-colors" title="Email: evasinghwork@gmail.com" aria-label="Email">
           <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
        </a>
        <a href="tel:+13199361467" class="text-gray-400 hover:text-white p-2 transition-colors" title="Call: +1 (319) 936-1467" aria-label="Phone">
           <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/></svg>
        </a>
      </div>
    </div>
    
    <div class="flex-1 flex justify-center md:justify-end">
      <!-- Cute Terminal Graphic -->
      <div class="relative w-72 h-56 bg-gray-900 rounded-lg retro-border overflow-hidden group">
        <div class="bg-gray-800 px-4 py-2 flex items-center gap-2 border-b border-gray-700">
          <div class="w-3 h-3 rounded-full bg-red-500"></div>
          <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
          <div class="w-3 h-3 rounded-full bg-green-500"></div>
          <div class="text-xs text-gray-400 ml-2 font-mono">eva@iowa: ~</div>
        </div>
        <div class="p-4 font-mono text-sm">
          <div class="text-iowa-gold mb-1">$ ./init_portfolio.sh</div>
          <div class="text-gray-300 mb-1">> Loading skills... [OK]</div>
          <div class="text-gray-300 mb-1">> Compiling awesomeness... [OK]</div>
          <div class="text-green-400 mb-4">> Ready to build.</div>
          <div class="flex items-center gap-1">
            <span class="text-iowa-gold">$</span> 
            <span class="w-2 h-4 bg-gray-400 animate-pulse"></span>
          </div>
        </div>
        <!-- Decorative pixel stars -->
        <div class="absolute top-10 right-4 text-iowa-gold opacity-50 group-hover:opacity-100 transition-opacity">✦</div>
        <div class="absolute bottom-6 left-12 text-iowa-gold opacity-30 group-hover:opacity-80 transition-opacity text-xs">★</div>
      </div>
    </div>
  </section>
</template>

