<script setup>
const name = 'Husseen Aden'
const profession = 'Front-End Developer'
const location = 'Rotterdam, The Netherlands'
const resumeLink = '../assets/HusseenAden_Resume.pdf'
</script>

<template>
  <section class="max-w-4xl mx-auto px-6 py-12 flex flex-col md:flex-row items-center gap-10">
    <div class="flex-1 text-center md:text-left">
      <h1 class="text-4xl font-bold mb-4 text-gray-800">
        {{ name }}
      </h1>
      <h2 class="text-2xl font-semibold mb-2 text-gray-600">
        {{ profession }}
      </h2>
      <p class="text-lg text-gray-600 mb-4">
        {{ location }}
      </p>
      <a
        :href="resumeLink"
        download
        class="inline-block mt-4 px-6 py-3 bg-blue-600 text-white rounded hover:bg-blue-700 transition-colors duration-300"
      >
        Download Resume
      </a>
    </div>

    <div class="shrink-0">
      <img
        src="../assets/placeholder-2-1.webp"
        alt="Profielfoto"
        class="h-48 w-48 rounded-4xl object-cover shadow-lg border border-gray-200"
      />
    </div>
  </section>
</template>
