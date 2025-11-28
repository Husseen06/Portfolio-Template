<script setup>
import { ref } from 'vue'
const about = ref([
  {
    title: 'Who I Am',
    description:
      'My name is Husseen Aden, a passionate front-end developer with a strong foundation in web technologies. I specialize in creating responsive and user-friendly web applications using modern frameworks and tools.',
  },
])
const workExperience = ref([
  {
    position: 'Front-End Developer Intern',
    company: 'Tech Placeholder Inc.',
    duration: 'June 2022 - August 2022',
    description:
      'I have worked on various projects ranging from small business websites to complex web applications. My experience includes collaborating with cross-functional teams, implementing responsive designs, and optimizing web performance to enhance user experience.',
  },
])
</script>

<template>
  <section class="max-w-6xl mx-auto px-6 py-12">
    <h2 class="text-3xl font-bold mb-8 text-gray-800 text-center">About</h2>
    <div class="mb-12">
      <div
        v-for="(item, index) in about"
        :key="index"
        class="bg-white rounded-lg shadow-md p-6 hover:shadow-xl transition-shadow duration-300"
      >
        <h3 class="text-xl font-semibold mb-2 text-gray-800">
          {{ item.title }}
        </h3>
        <p class="text-gray-600">
          {{ item.description }}
        </p>
      </div>
    </div>

    <div class="shrink-0">
      <h2 class="text-3xl font-bold mb-8 text-gray-800 text-center mt-12">Work Experience</h2>

      <div
        v-for="(work, index) in workExperience"
        :key="index"
        class="bg-white rounded-lg shadow-md p-6 mb-6 hover:shadow-xl transition-shadow duration-300"
      >
        <h3 class="text-xl font-semibold mb-2 text-gray-800">
          {{ work.position }} - {{ work.company }}
        </h3>
        <p class="text-gray-600 italic mb-2">
          {{ work.duration }}
        </p>
        <p class="text-gray-600">
          {{ work.description }}
        </p>
      </div>
    </div>
  </section>
</template>
