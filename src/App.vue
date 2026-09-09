<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Experience from './components/Experience.vue'
import Projects from './components/Projects.vue'
import FeaturedIn from './components/FeaturedIn.vue'
import Awards from './components/Awards.vue'
import Involvement from './components/Involvement.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="min-h-screen bg-iowa-black text-gray-200">
    <Navbar />
    <main class="max-w-5xl mx-auto px-6 py-12 md:py-24 space-y-32">
      <Hero />
      <About id="about" />
      <Experience id="experience" />
      <Projects id="projects" />
      <FeaturedIn id="featured" />
      <Awards id="awards" />
      <Involvement id="involvement" />
      <Skills id="skills" />
      <Contact id="contact" />
    </main>
    <Footer />
  </div>
</template>
