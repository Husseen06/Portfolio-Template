<script setup>
import project1Image from '../assets/placeholder-2-1.webp'

const projects = [
  {
    title: 'Project One',
    description: 'A brief description of Project One.',
    tags: ['HTML', 'CSS', 'JavaScript'],
    imageUrl: project1Image,
    caseStudyLink: '#',
  },
  {
    title: 'Project Two',
    description: 'A brief description of Project Two.',
    tags: ['Vue', 'Tailwind', 'JS'],
    imageUrl: project1Image,
    caseStudyLink: '#',
  },
  {
    title: 'Project Three',
    description: 'A brief description of Project Three.',
    tags: ['CSS', 'Responsive', 'JS'],
    imageUrl: project1Image,
    caseStudyLink: '#',
  },
]
</script>

<template>
  <section id="projects" class="max-w-6xl mx-auto px-6 py-12 bg-blue-50">
    <h2 class="text-3xl font-bold mb-8 text-center text-gray-800">Projects</h2>
    <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300"
      >
        <img :src="project.imageUrl" :alt="project.title" class="w-full h-48 object-cover" />
        <div class="p-6">
          <h3 class="text-xl font-semibold mb-2 text-blue-800">{{ project.title }}</h3>
          <p class="text-blue-700 mb-4">{{ project.description }}</p>
          <div class="flex flex-wrap gap-2 mb-4">
            <span
              v-for="tag in project.tags"
              :key="tag"
              class="bg-blue-200 text-blue-800 text-xs px-2 py-1 rounded-full"
            >
              {{ tag }}
            </span>
          </div>
          <a :href="project.caseStudyLink" class="text-blue-500 hover:underline"> View Project </a>
        </div>
      </div>
    </div>
  </section>
</template>
