<script setup>
import { ref } from 'vue'

const isMobileMenuOpen = ref(false)

const links = [
  { name: 'Home', href: '#' },
  { name: 'Experience', href: '#experience' },
  { name: 'Projects', href: '#projects' },
  { name: 'Featured In', href: '#featured' },
  { name: 'Awards', href: '#awards' },
  { name: 'Involvement', href: '#involvement' },
  { name: 'Skills', href: '#skills' },
  { name: 'Resume', href: '/resume.pdf' }
]
</script>

<template>
  <header class="sticky top-0 z-50 bg-iowa-black/90 backdrop-blur-sm border-b border-gray-800">
    <div class="max-w-7xl mx-auto px-6 h-16 flex items-center justify-between">
      <div class="font-mono text-iowa-gold font-bold text-xl tracking-tight">
        <a href="#">Eva Singh</a>
      </div>
      
      <!-- Desktop Nav -->
      <nav class="hidden md:flex gap-6">
        <a 
          v-for="link in links" 
          :key="link.name" 
          :href="link.href"
          class="text-sm hover:text-iowa-gold transition-colors"
          :target="link.name === 'Resume' ? '_blank' : undefined"
        >
          {{ link.name }}
        </a>
      </nav>

      <!-- Mobile Menu Button -->
      <button 
        @click="isMobileMenuOpen = !isMobileMenuOpen" 
        class="md:hidden text-gray-200 hover:text-iowa-gold focus:outline-none"
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                :d="isMobileMenuOpen ? 'M6 18L18 6M6 6l12 12' : 'M4 6h16M4 12h16M4 18h16'"/>
        </svg>
      </button>
    </div>

    <!-- Mobile Nav -->
    <nav v-show="isMobileMenuOpen" class="md:hidden bg-iowa-black border-b border-gray-800 px-6 py-4 flex flex-col gap-4">
      <a 
        v-for="link in links" 
        :key="link.name" 
        :href="link.href"
        class="text-sm hover:text-iowa-gold transition-colors"
        @click="isMobileMenuOpen = false"
        :target="link.name === 'Resume' ? '_blank' : undefined"
      >
        {{ link.name }}
      </a>
    </nav>
  </header>
</template>

