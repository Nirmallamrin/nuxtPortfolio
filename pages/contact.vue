<template>
    <div class="bg-gray-100 p-8">
      <h1 class="font-bold italic text-gray-900 text-5xl text-center mb-12">Contact Me</h1>
      <div class="container mx-auto flex flex-col md:flex-row justify-between">
        <!-- Left Section (Contact Form) -->
        <div class="md:w-2/3">
          <form @submit.prevent="handleSubmit" class="bg-white p-6 rounded-lg shadow-lg">
            <div class="mb-4">
              <label for="name" class="block text-gray-700 text-sm font-bold mb-2">Name</label>
              <input 
                type="text" 
                id="name" 
                v-model="name" 
                class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                required
              />
            </div>
            <div class="mb-4">
              <label for="email" class="block text-gray-700 text-sm font-bold mb-2">Email</label>
              <input 
                type="email" 
                id="email" 
                v-model="email" 
                class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                required
              />
            </div>
            <div class="mb-4">
              <label for="message" class="block text-gray-700 text-sm font-bold mb-2">Message</label>
              <textarea 
                id="message" 
                v-model="message" 
                rows="4" 
                class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                required
              ></textarea>
            </div>
            <button 
              type="submit" 
              class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
            >
              Send Message
            </button>
          </form>
        </div>
  
        <!-- Right Section (Contact Details) -->
        <div class="md:w-1/3 md:ml-8 mt-8 md:mt-0">
          <h2 class="text-xl font-bold mb-4">Get in Touch</h2>
          <p class="text-gray-700 mb-2">Email: <a href="mailto:your-email@example.com" class="text-blue-500 hover:underline">your-email@example.com</a></p>
          <p class="text-gray-700 mb-2">Phone: <span class="text-blue-500">+123 456 7890</span></p>
          <p class="text-gray-700 mb-2">LinkedIn: <a href="https://linkedin.com/in/yourprofile" target="_blank" class="text-blue-500 hover:underline">yourprofile</a></p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const name = ref('');
  const email = ref('');
  const message = ref('');
  
  const handleSubmit = () => {
    // Handle form submission (e.g., send data to an API)
    alert(`Message sent from: ${name.value}, Email: ${email.value}, Message: ${message.value}`);
    
    // Clear form fields
    name.value = '';
    email.value = '';
    message.value = '';
  };
  </script>
  
  <style scoped>
  </style>
  