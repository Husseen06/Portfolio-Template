<script setup>
import summaryImage from '../assets/placeholder-2-1.webp'
const title = 'Frontend Developer'
const imageUrl = summaryImage
const location = 'City, Country'
const resumeLink = '#'
</script>

<template>
  <section
    id="home"
    class="max-w-5xl mx-auto px-6 py-20 flex flex-col md:flex-row items-center gap-10 bg-blue-50 rounded-xl shadow-lg"
  >
    <div class="flex-1 text-center md:text-left">
      <h1 class="text-5xl font-bold mb-4 text-gray-800">Portfolio</h1>
      <h2 class="text-2xl font-semibold mb-2 text-blue-800">{{ title }}</h2>
      <p class="text-lg mb-6 text-blue-700">{{ location }}</p>
      <a
        :href="resumeLink"
        download
        class="inline-block mt-4 px-8 py-3 bg-blue-500 text-white font-semibold rounded-full shadow hover:bg-blue-600 transition-colors duration-300"
      >
        Download Resume
      </a>
    </div>
    <div class="flex-shrink-0">
      <img
        :src="imageUrl"
        alt="Profile Picture"
        class="h-48 w-48 md:h-56 md:w-56 rounded-full object-cover shadow-xl border-4 border-blue-200"
      />
    </div>
  </section>
</template>
