<script setup>
import placeholderImage from '../assets/placeholder-2-1.webp'

const about = [
  {
    title: 'Who I Am',
    description:
      'I am a passionate front-end developer creating responsive and user-friendly web applications with modern frameworks and tools.',
  },
]

const workExperience = [
  {
    position: 'Frontend Developer Intern',
    company: 'Tech Company',
    duration: 'June 2022 - August 2022',
    description:
      'Worked on multiple projects implementing responsive designs, optimizing performance, and collaborating with cross-functional teams.',
    imageUrl: placeholderImage,
  },
]

const education = [
  {
    school: 'University of Technology',
    degree: 'B.Sc. in Computer Science',
    duration: '2018 - 2022',
    description: 'Focused on web development, software engineering, and database management.',
    imageUrl: placeholderImage,
  },
]
</script>

<template>
  <section id="about" class="max-w-6xl mx-auto px-6 py-12 bg-white text-gray-800">
    <h2 class="text-3xl font-bold mb-8 text-center text-gray-800">About</h2>

    <div class="space-y-6">
      <div
        v-for="(item, index) in about"
        :key="index"
        class="bg-blue-50 rounded-lg shadow-md p-6 hover:shadow-xl transition-shadow duration-300"
      >
        <h3 class="text-xl font-semibold mb-2 text-blue-800">{{ item.title }}</h3>
        <p class="text-blue-700">{{ item.description }}</p>
      </div>
    </div>

    <h2 class="text-3xl font-bold mt-12 mb-8 text-center text-gray-800">Work Experience</h2>
    <div class="space-y-6">
      <div
        v-for="(work, index) in workExperience"
        :key="index"
        class="bg-blue-50 rounded-lg shadow-md p-6 hover:shadow-xl transition-shadow duration-300 flex flex-col sm:flex-row items-center gap-6"
      >
        <img
          :src="work.imageUrl"
          :alt="work.company"
          class="w-24 h-24 rounded-full object-cover border-4 border-blue-200 flex-shrink-0"
        />
        <div class="text-center sm:text-left">
          <h3 class="text-xl font-semibold mb-1 text-blue-800">
            {{ work.position }} - {{ work.company }}
          </h3>
          <p class="italic mb-2 text-blue-700">{{ work.duration }}</p>
          <p class="text-blue-700">{{ work.description }}</p>
        </div>
      </div>
    </div>

    <h2 class="text-3xl font-bold mt-12 mb-8 text-center text-gray-800">Education</h2>
    <div class="space-y-6">
      <div
        v-for="(edu, index) in education"
        :key="index"
        class="bg-blue-50 rounded-lg shadow-md p-6 hover:shadow-xl transition-shadow duration-300 flex flex-col sm:flex-row items-center gap-6"
      >
        <img
          :src="edu.imageUrl"
          :alt="edu.school"
          class="w-24 h-24 rounded-full object-cover border-4 border-blue-200 flex-shrink-0"
        />
        <div class="text-center sm:text-left">
          <h3 class="text-xl font-semibold mb-1 text-blue-800">{{ edu.school }}</h3>
          <p class="italic mb-2 text-blue-700">{{ edu.degree }} ({{ edu.duration }})</p>
          <p class="text-blue-700">{{ edu.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
