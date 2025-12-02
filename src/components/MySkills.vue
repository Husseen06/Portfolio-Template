<script setup>
const skills = [
  { name: 'HTML', icon: ['fab', 'html5'], description: 'Semantic HTML for accessible content.' },
  { name: 'CSS', icon: ['fab', 'css3-alt'], description: 'Modern CSS with Flexbox & Grid.' },
  { name: 'JavaScript', icon: ['fab', 'js'], description: 'Dynamic and interactive features.' },
  { name: 'Vue.js', icon: ['fab', 'vuejs'], description: 'Reactive UI with Vue.js.' },
  { name: 'PHP', icon: ['fab', 'php'], description: 'Backend scripting & database work.' },
  { name: 'WordPress', icon: ['fab', 'wordpress'], description: 'CMS and site building.' },
  { name: 'Git', icon: ['fab', 'git-alt'], description: 'Version control and collaboration.' },
  { name: 'Figma', icon: ['fas', 'palette'], description: 'UI/UX design prototyping.' },
  { name: 'Scrum', icon: ['fas', 'users'], description: 'Agile development methodology.' },
]
</script>

<template>
  <section id="skills" class="max-w-6xl mx-auto px-6 py-12 bg-blue-50">
    <h2 class="text-3xl font-bold mb-8 text-center text-gray-800">Skills</h2>
    <div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
      <div
        v-for="(skill, index) in skills"
        :key="index"
        class="bg-white rounded-lg shadow-md p-6 hover:shadow-xl transition-shadow duration-300 flex flex-col items-center text-center"
      >
        <font-awesome-icon :icon="skill.icon" class="text-5xl mb-4 text-blue-600" />
        <h3 class="text-xl font-semibold mb-2 text-blue-800">{{ skill.name }}</h3>
        <p class="text-blue-700">{{ skill.description }}</p>
      </div>
    </div>
  </section>
</template>
