<script setup>
import { featured } from '../data/featured.js'
</script>

<template>
  <section class="space-y-8">
    <div class="flex items-center gap-4 mb-12">
      <h2 class="text-3xl font-bold font-mono text-white">
        <span class="text-iowa-gold">04.</span> Featured In
      </h2>
      <div class="h-px bg-gray-700 flex-1"></div>
    </div>

    <div class="space-y-6">
      <div 
        v-for="item in featured" 
        :key="item.id" 
        class="bg-gray-900/80 border border-gray-800 rounded-lg p-6 md:p-8 flex flex-col md:flex-row md:items-center justify-between gap-6 hover:border-iowa-gold/50 transition-all hover-lift"
      >
        <div class="flex-1">
          <div class="text-iowa-gold font-mono text-xs sm:text-sm mb-2 font-semibold">
            {{ item.publication }} &mdash; {{ item.date }}
          </div>
          <h3 class="text-xl font-bold text-white mb-3 hover:text-iowa-gold transition-colors">
            {{ item.title }}
          </h3>
          <p class="text-gray-400 text-sm max-w-2xl leading-relaxed">
            {{ item.description }}
          </p>
        </div>
        
        <a 
          :href="item.url" 
          target="_blank" 
          rel="noopener noreferrer"
          class="inline-flex items-center gap-2 text-sm font-bold text-black bg-iowa-gold hover:bg-yellow-400 px-5 py-2.5 rounded transition-colors whitespace-nowrap self-start md:self-auto"
        >
          Read Article
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
        </a>
      </div>
    </div>
  </section>
</template>
