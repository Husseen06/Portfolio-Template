<script setup>
import { ref } from 'vue'

const navItems = [
  { name: 'Home', href: '#home' },
  { name: 'About', href: '#about' },
  { name: 'Skills', href: '#skills' },
  { name: 'Projects', href: '#projects' },
  { name: 'Contact', href: '#contact' },
]

const isMobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}
</script>

<template>
  <nav class="bg-blue-100 shadow-md sticky top-0 z-50">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex justify-between items-center h-16">
        <a href="#home" class="text-2xl font-bold text-blue-800">Portfolio</a>

        <!-- Hamburger icon for mobile -->
        <div class="md:hidden">
          <button @click="toggleMobileMenu" class="text-blue-700 focus:outline-none">
            <svg
              class="w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              ></path>
            </svg>
          </button>
        </div>

        <div class="hidden md:flex space-x-6">
          <a
            v-for="(item, index) in navItems"
            :key="index"
            :href="item.href"
            class="text-blue-700 hover:text-blue-500 transition-colors"
          >
            {{ item.name }}
          </a>
        </div>
      </div>
    </div>

    <!-- Mobile menu -->
    <div v-if="isMobileMenuOpen" class="md:hidden bg-blue-50 py-4 px-6">
      <div class="flex flex-col space-y-4">
        <a
          v-for="(item, index) in navItems"
          :key="index"
          :href="item.href"
          @click="closeMobileMenu"
          class="text-blue-700 hover:text-blue-500 transition-colors text-lg"
        >
          {{ item.name }}
        </a>
      </div>
    </div>
  </nav>
</template>
