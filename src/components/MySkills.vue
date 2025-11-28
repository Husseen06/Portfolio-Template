<script setup>
import { ref } from 'vue'

const skills = ref([
  {
    name: 'HTML',
    description:
      'Structuring web content with semantic HTML5 elements for better accessibility and SEO.',
  },
  {
    name: 'CSS',
    description:
      'Styling web pages with modern CSS techniques including Flexbox and Grid for responsive design.',
  },
  {
    name: 'JavaScript',
    description: 'Implementing interactive features and dynamic content using vanilla JavaScript.',
  },
  {
    name: 'Vue.js',
    description: 'Building dynamic and reactive user interfaces using the Vue.js framework.',
  },
  {
    name: 'Tailwind CSS',
    description: 'Creating responsive and modern designs using utility-first CSS framework.',
  },
  {
    name: 'Axios',
    description: 'Handling HTTP requests and responses for seamless data integration.',
  },
  {
    name: 'PHP & MySQL',
    description: 'Server-side scripting and database management for dynamic web content.',
  },
  {
    name: 'Git & GitHub',
    description: 'Version control and team collaboration with Git best practices.',
  },
  {
    name: 'Figma',
    description: 'Designing user interfaces and experiences with collaborative tools.',
  },
])
</script>

<template>
  <section class="max-w-6xl mx-auto px-6 py-12">
    <h2 class="text-3xl font-bold mb-8 text-gray-800 text-center">My Skills</h2>
    <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
      <div
        v-for="(skill, index) in skills"
        :key="index"
        class="bg-white rounded-lg shadow-md p-6 hover:shadow-xl transition-shadow duration-300"
      >
        <h3 class="text-xl font-semibold mb-2 text-gray-800">
          {{ skill.name }}
        </h3>
        <p class="text-gray-600">
          {{ skill.description }}
        </p>
      </div>
    </div>
  </section>
</template>
