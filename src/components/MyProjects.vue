<script setup>
import { ref } from 'vue'

const projects = ref([
  {
    title: 'Project One',
    description: 'A brief description of Project One.',
    tags: ['HTML', 'CSS', 'JavaScript'],
    imageUrl: '../assets/project1.webp',
    caseStudyLink: '#',
  },
  {
    title: 'Project Two',
    description: 'A brief description of Project Two.',
    tags: ['HTML', 'CSS', 'JavaScript'],
    imageUrl: '../assets/project2.webp',
    caseStudyLink: '#',
  },
  {
    title: 'Project Three',
    description: 'A brief description of Project Three.',
    tags: ['HTML', 'CSS', 'JavaScript'],
    imageUrl: '../assets/project3.webp',
    caseStudyLink: '#',
  },
])
</script>

<template>
  <section>
    <div class="max-w-6xl mx-auto px-6 py-12">
      <h2 class="text-3xl font-bold mb-8 text-gray-800 text-center">My Projects</h2>
      <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300"
        >
          <img :src="project.imageUrl" :alt="project.title" class="w-full h-48 object-cover" />
          <div class="p-6">
            <h3 class="text-xl font-semibold mb-2 text-gray-800">
              {{ project.title }}
            </h3>
            <p class="text-gray-600 mb-4">
              {{ project.description }}
            </p>
            <div class="mb-4">
              <span
                v-for="(tag, tagIndex) in project.tags"
                :key="tagIndex"
                class="inline-block bg-blue-100 text-blue-800 text-xs px-2 py-1 rounded-full mr-2"
              >
                {{ tag }}
              </span>
            </div>
            <a :href="project.caseStudyLink" class="text-blue-600 hover:underline">
              View Project
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
