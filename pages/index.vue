<template>
  <div class="min-h-screen bg-gray-950 flex items-center justify-center">
    <div class="container px-8 md:px-12 flex flex-col-reverse md:flex-row  justify-between md:justify-center space-y-8 md:space-y-0 md:space-x-12">
      <!-- Left Section (Name and Profession) -->
      <div class="md:w-1/2 flex flex-col items-center md:items-start text-center md:text-left">
        <h1 class="text-5xl md:text-6xl font-bold text-white">My name is Nirmal</h1>
        <p class="text-lg md:text-2xl text-white mt-4">I am a skilled Software Developer specializing in building efficient and scalable applications.</p>

        <div class="flex mt-6 space-x-6">
          <a href="https://www.linkedin.com/in/nirmal-mani-399125268/" target="_blank" class="text-white hover:text-gray-400">
            <i class="fab fa-linkedin fa-2x"></i>
          </a>
          <a href="https://github.com/Nirmallamrin" target="_blank" class="text-white hover:text-gray-400">
            <i class="fab fa-github fa-2x"></i>
          </a>
          <a href="https://www.instagram.com/lamrin_____6/?hl=en" target="_blank" class="text-white hover:text-gray-400">
            <i class="fab fa-instagram fa-2x"></i>
          </a>
          <a href="https://facebook.com" target="_blank" class="text-white hover:text-gray-400">
            <i class="fab fa-facebook fa-2x"></i>
          </a>
          <a href="https://twitter.com" target="_blank" class="text-white hover:text-gray-400">
            <i class="fab fa-twitter fa-2x"></i>
          </a>
        </div>
      </div>

      <!-- Right Section (Image) -->
      <div class="w-80 h-80 md:w-80 md:h-80">
        <img 
          src="/_nuxt/assets/IMG03.jpeg" 
          alt="Nirmal's Image" 
          class="object-cover w-full h-full rounded-full shadow-lg"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
</script>
