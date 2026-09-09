<script setup>
import { involvement } from '../data/involvement.js'
</script>

<template>
  <section class="space-y-8">
    <div class="flex items-center gap-4 mb-12">
      <h2 class="text-3xl font-bold font-mono text-white">
        <span class="text-iowa-gold">06.</span> Leadership & Involvement
      </h2>
      <div class="h-px bg-gray-700 flex-1"></div>
    </div>

    <div class="grid md:grid-cols-2 gap-6">
      <div 
        v-for="item in involvement" 
        :key="item.id" 
        class="bg-gray-900/80 border border-gray-800 rounded-lg p-6 hover:border-iowa-gold/50 transition-all hover-lift flex flex-col justify-between"
      >
        <div class="space-y-3">
          <div class="flex items-center justify-between">
            <span class="text-xs font-mono text-iowa-gold bg-iowa-gold/10 px-2.5 py-1 rounded border border-iowa-gold/20">
              {{ item.date }}
            </span>
          </div>
          <div>
            <h3 class="text-lg font-bold text-white">{{ item.role }}</h3>
            <p class="text-sm text-gray-400 font-medium">{{ item.organization }}</p>
          </div>
          <ul class="space-y-1.5 text-gray-300 text-sm list-disc list-inside marker:text-iowa-gold">
            <li v-for="(desc, idx) in item.description" :key="idx" class="leading-relaxed">
              {{ desc }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

