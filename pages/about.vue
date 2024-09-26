<template>
  <div class="min-h-screen bg-gray-950 flex items-center justify-center px-4">
    <div class="container mx-auto flex flex-col itemsmd:flex-row items-center space-y-8 md:space-y-0 md:space-x-8 text-center md:text-left">
      
      <!-- Left Section (Photo) -->
      <div class="w-40 h-40 md:w-60 md:h-60">
        <img 
          src="/IMG02.jpeg" 
          alt="Nirmal's Photo" 
          class="rounded-full shadow-lg object-cover w-full h-full border-4 border-white"
        />
      </div>

      <!-- Right Section (About Me Paragraph) -->
      <div class="max-w-md">
        <h1 class="text-4xl font-bold text-white mb-4">About Me</h1>
        <p class="text-lg text-gray-300 leading-relaxed">
          Hello, I'm Nirmal, a dedicated Software Developer with experience in building full-stack applications. 
          I specialize in creating efficient and scalable solutions using the MERN stack. Always eager to learn and 
          contribute to meaningful projects, I am passionate about delivering high-quality software and embracing modern 
          web technologies.
        </p>
      </div>
      
    </div>
  </div>
</template>

<script setup>
</script>
