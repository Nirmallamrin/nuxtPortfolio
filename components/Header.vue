<template>
    <header class="bg-gray-900 text-white py-4">
      <div class="container mx-auto flex justify-between items-center px-12 py-2">
        <!-- Left Section (About Me Title) -->
        <NuxtLink to="/" class="text-3xl font-extrabold ml-12">About Me</NuxtLink>
  
        <!-- Hamburger Icon (for mobile) -->
        <div class="md:hidden">
          <button @click="toggleMenu" class="focus:outline-none">
            <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
  
        <!-- Right Section (Navigation Links) - hidden on small screens -->
        <nav :class="{'hidden': !isMenuOpen, 'block': isMenuOpen }" class="text-xl hidden md:flex space-x-6 mr-12">
          <NuxtLink to="/" class="hover:text-gray-400">Home</NuxtLink>
          <NuxtLink to="/about" class="hover:text-gray-400">About</NuxtLink>
          <NuxtLink to="/projects" class="hover:text-gray-400">Projects</NuxtLink>
          <NuxtLink to="/skills" class="hover:text-gray-400">Skills</NuxtLink>
          <NuxtLink to="/resume" class="block hover:text-gray-400">Resume</NuxtLink>
          <NuxtLink to="/contact" class="hover:text-gray-400">Contact</NuxtLink>
        </nav>
      </div>
  
      <!-- Mobile Menu (only visible on small screens) -->
      <div v-if="isMenuOpen" class="md:hidden">
        <nav class="px-4 py-2 space-y-2 bg-gray-800">
          <NuxtLink to="/" class="block hover:text-gray-400">Home</NuxtLink>
          <NuxtLink to="/about" class="block hover:text-gray-400">About</NuxtLink>
          <NuxtLink to="/projects" class="block hover:text-gray-400">Projects</NuxtLink>
          <NuxtLink to="/skills" class="block hover:text-gray-400">Skills</NuxtLink>
          <NuxtLink to="/contact" class="block hover:text-gray-400">Resume</NuxtLink>
          <NuxtLink to="/contact" class="block hover:text-gray-400">Contact</NuxtLink>
        </nav>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isMenuOpen: false
      }
    },
    methods: {
      toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen
      }
    }
  }
  </script>
  