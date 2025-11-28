<script setup>
import { ref } from 'vue'

const navItems = ref([
  { name: 'Home', href: '#home' },
  { name: 'About', href: '#about' },
  { name: 'Experience', href: '#experience' },
  { name: 'Skills', href: '#skills' },
  { name: 'Projects', href: '#projects' },
  { name: 'Contact', href: '#contact' },
])
</script>

<template>
  <nav class="bg-white shadow-md">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex justify-between">
        <div class="flex space-x-4">
          <div>
            <a href="#home" class="flex items-center py-5 px-2 text-gray-700 hover:text-gray-900">
              <span class="font-bold text-xl">MyPortfolio</span>
            </a>
          </div>
          <div class="hidden md:flex items-center space-x-1">
            <a
              v-for="(item, index) in navItems"
              :key="index"
              :href="item.href"
              class="py-5 px-3 text-gray-700 hover:text-gray-900"
            >
              {{ item.name }}
            </a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
