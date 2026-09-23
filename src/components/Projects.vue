<script setup>
import { projects } from '../data/projects.js'
</script>

<template>
  <section class="space-y-8">
    <div class="flex items-center gap-4 mb-12">
      <h2 class="text-3xl font-bold font-mono text-white">
        <span class="text-iowa-gold">03.</span> Projects
      </h2>
      <div class="h-px bg-gray-700 flex-1"></div>
    </div>

    <div class="grid md:grid-cols-2 gap-6">
      <div 
        v-for="project in projects" 
        :key="project.id" 
        class="bg-gray-900/80 border border-gray-800 rounded-lg p-6 flex flex-col hover-lift relative group hover:border-iowa-gold/50 transition-all justify-between"
      >
        <div>
          <!-- Header with Folder icon & Top-right Action Icons -->
          <div class="flex justify-between items-center mb-6">
            <div class="text-iowa-gold">
              <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z"></path>
              </svg>
            </div>
            
            <div class="flex items-center gap-3">
              <!-- Live Site Icon -->
              <a 
                v-if="project.liveUrl" 
                :href="project.liveUrl" 
                target="_blank" 
                rel="noopener noreferrer"
                class="text-gray-400 hover:text-iowa-gold transition-colors p-1"
                title="View Live Site"
                aria-label="Live Demo"
              >
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"></path>
                </svg>
              </a>
            </div>
          </div>
          
          <h3 class="text-xl font-bold text-white mb-2 group-hover:text-iowa-gold transition-colors">
            {{ project.title }}
          </h3>
          <p class="text-gray-400 text-sm leading-relaxed mb-4">
            {{ project.description }}
          </p>

          <!-- Prominent Call-to-Action Button for Videos / Links -->
          <div class="flex flex-wrap gap-3 my-4">
            <a 
              v-if="project.videoUrl" 
              :href="project.videoUrl" 
              target="_blank" 
              rel="noopener noreferrer"
              class="inline-flex items-center gap-2 px-4 py-2 bg-iowa-gold text-black rounded font-bold text-xs hover:bg-yellow-400 transition-all shadow-md shadow-iowa-gold/10"
            >
              <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                <path d="M8 5v14l11-7z"/>
              </svg>
              Watch Demo Video
            </a>

            <a 
              v-if="project.githubUrl" 
              :href="project.githubUrl" 
              target="_blank" 
              rel="noopener noreferrer"
              class="inline-flex items-center gap-2 px-3 py-1.5 border border-gray-700 text-gray-300 rounded text-xs font-mono hover:border-iowa-gold hover:text-iowa-gold transition-all"
            >
              GitHub Repo
            </a>
          </div>
        </div>
        
        <!-- Technology tags at bottom of card -->
        <ul class="flex flex-wrap gap-2 text-xs font-mono text-gray-500 mt-4 pt-4 border-t border-gray-800/80">
          <li v-for="tech in project.technologies" :key="tech" class="bg-gray-800/80 px-2.5 py-1 rounded text-gray-400 border border-gray-700/50">
            {{ tech }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
