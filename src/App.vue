<script setup>
import Navbar from './components/NavbarItem.vue'
import About from './components/AboutMe.vue'
import Skills from './components/MySkills.vue'
import Project from './components/MyProjects.vue'
import Contact from './components/ContactMe.vue'
import SummaryItem from './components/SummaryItem.vue'
</script>

<template>
  <Navbar />
  <main class="mt-16">
    <SummaryItem />
    <About />
    <Skills />
    <Project />
    <Contact />
  </main>
</template>

<style>
html {
  scroll-behavior: smooth;
  scroll-padding-top: 4rem; /* 16 (h-16 on navbar) * 0.25rem = 4rem */
}
</style>
