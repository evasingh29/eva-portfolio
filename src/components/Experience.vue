<script setup>
import { experience } from '../data/experience.js'
</script>

<template>
  <section class="space-y-8">
    <div class="flex items-center gap-4 mb-12">
      <h2 class="text-3xl font-bold font-mono text-white">
        <span class="text-iowa-gold">02.</span> Experience
      </h2>
      <div class="h-px bg-gray-700 flex-1"></div>
    </div>

    <div class="space-y-12">
      <div v-for="job in experience" :key="job.id" class="relative pl-8 md:pl-0">
        <!-- Timeline line for mobile -->
        <div class="md:hidden absolute left-0 top-0 bottom-0 w-px bg-gray-700"></div>
        <div class="md:hidden absolute left-[-4px] top-2 w-2 h-2 rounded-full bg-iowa-gold"></div>

        <div class="md:grid md:grid-cols-4 gap-8 group">
          <div class="mb-2 md:mb-0 text-sm font-mono text-gray-400 pt-1 group-hover:text-iowa-gold transition-colors">
            {{ job.date }}
          </div>
          
          <div class="md:col-span-3 space-y-4">
            <div>
              <h3 class="text-xl font-bold text-white">{{ job.position }}</h3>
              <p class="text-iowa-gold font-medium">{{ job.company }}</p>
            </div>
            
            <ul class="space-y-2 text-gray-300 list-disc list-inside marker:text-iowa-gold">
              <li v-for="(desc, index) in job.description" :key="index" class="pl-2">
                <span class="-ml-2">{{ desc }}</span>
              </li>
            </ul>

            <div class="flex flex-wrap gap-2 pt-2">
              <span v-for="tech in job.technologies" :key="tech" class="px-3 py-1 bg-gray-800 text-iowa-gold text-xs rounded-full font-mono border border-gray-700">
                {{ tech }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

