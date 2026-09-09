<script setup>
import { awards } from '../data/awards.js'
</script>

<template>
  <section class="space-y-8">
    <div class="flex items-center gap-4 mb-12">
      <h2 class="text-3xl font-bold font-mono text-white">
        <span class="text-iowa-gold">05.</span> Honors & Awards
      </h2>
      <div class="h-px bg-gray-700 flex-1"></div>
    </div>

    <div class="grid md:grid-cols-2 gap-6">
      <div v-for="award in awards" :key="award.id" 
           class="p-6 bg-gray-900/80 border border-gray-800 rounded-lg border-l-4 border-l-iowa-gold flex flex-col justify-center hover-lift transition-all">
        <div class="font-mono text-iowa-gold text-xs font-semibold mb-1">{{ award.date }}</div>
        <h3 class="text-lg font-bold text-white mb-2">{{ award.title }}</h3>
        <p class="text-gray-400 text-sm leading-relaxed">{{ award.description }}</p>
      </div>
    </div>
  </section>
</template>
