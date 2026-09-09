<script setup>
const skills = [
  {
    category: 'Languages & Frameworks',
    items: ['Python', 'PyTorch', 'Java', 'C++', 'C#', 'SQL', 'TypeScript', 'Vue 3', 'Flask', 'React', 'Socket.IO']
  },
  {
    category: 'Machine Learning & AI',
    items: ['scikit-learn', 'Weights & Biases', 'MLflow', 'Jupyter', 'NumPy', 'pandas', 'GANs (WGANs)', 'Deep Learning', 'NLP', 'Sentiment Analysis', 'OpenAI API']
  },
  {
    category: 'Tools & Platforms',
    items: ['Git', 'Docker', 'AWS ECR', 'MongoDB', 'Unity', 'Postman', 'VS Code', 'IntelliJ IDEA', 'PyCharm', 'CLion']
  },
  {
    category: 'Professional & Leadership',
    items: ['Stakeholder Management', 'Cross-Functional Collaboration', 'Technical Communication', 'Project Management', 'Mentorship & Coaching', 'Strategic Planning']
  }
]
</script>

<template>
  <section class="space-y-8">
    <div class="flex items-center gap-4 mb-12">
      <h2 class="text-3xl font-bold font-mono text-white">
        <span class="text-iowa-gold">07.</span> Technical Skills
      </h2>
      <div class="h-px bg-gray-700 flex-1"></div>
    </div>

    <div class="grid md:grid-cols-2 gap-8">
      <div v-for="group in skills" :key="group.category" class="space-y-4">
        <h3 class="text-xl font-bold text-gray-200 border-b border-gray-800 pb-2 flex items-center gap-2">
          <svg class="w-5 h-5 text-iowa-gold" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
          {{ group.category }}
        </h3>
        <div class="flex flex-wrap gap-2">
          <span v-for="item in group.items" :key="item" 
                class="px-3 py-1.5 bg-gray-900 border border-gray-700 text-gray-300 rounded text-sm hover:border-iowa-gold hover:text-white cursor-default transition-colors font-mono">
            {{ item }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>
