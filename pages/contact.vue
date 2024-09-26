<template>
  <div class="bg-gray-950 py-16 px-4">
    <h1 class="font-bold italic text-white text-4xl text-center mb-12">Contact Me</h1>
    
    <div class="container mx-auto flex flex-col md:flex-row justify-center items-start space-y-8 md:space-y-0 md:space-x-8">
      
      <!-- Contact Form -->
      <div class="w-full md:w-1/2 lg:w-2/5">
        <form @submit.prevent="handleSubmit" class="bg-gray-900 p-6 rounded-lg shadow-lg space-y-4">
          <div>
            <label for="name" class="block text-white text-sm font-semibold mb-2">Your Name</label>
            <input 
              type="text" 
              id="name" 
              v-model="name" 
              class="shadow appearance-none border border-gray-300 rounded-md w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-400"
              placeholder="Enter your name"
              required
            />
          </div>
          
          <div>
            <label for="email" class="block text-white text-sm font-semibold mb-2">Email Address</label>
            <input 
              type="email" 
              id="email" 
              v-model="email" 
              class="shadow appearance-none border border-gray-300 rounded-md w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-400"
              placeholder="Enter your email"
              required
            />
          </div>
          
          <div>
            <label for="message" class="block text-white text-sm font-semibold mb-2">Message</label>
            <textarea 
              id="message" 
              v-model="message" 
              rows="4" 
              class="shadow appearance-none border border-gray-300 rounded-md w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-400"
              placeholder="Write your message here"
              required
            ></textarea>
          </div>
          
          <button 
            type="submit" 
            class="w-full bg-blue-500 hover:bg-blue-600 text-white font-semibold py-2 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-blue-400"
          >
            Send Message
          </button>
        </form>
      </div>

      <!-- Contact Details -->
      <div class="w-full md:w-1/2 lg:w-2/5 bg-gray-900 p-6 rounded-lg shadow-lg">
        <h2 class="text-2xl font-bold mb-6 text-white text-center md:text-left">Get in Touch</h2>
        <p class="text-white mb-4 text-center md:text-left">Feel free to reach out via email or phone, or connect with me on LinkedIn.</p>
        
        <div class="space-y-4 text-center md:text-left">
          <p class="text-white">
            <span class="font-semibold">Email:</span> 
            <a href="mailto:nirmallamrin77@gmail.com" class="text-blue-600 hover:underline">      nirmallamrin77@gmail.com</a>
          </p>
          
          <p class="text-white">
            <span class="font-semibold">Phone:</span> 
            <span class="text-blue-600">      +91 62826372247</span>
          </p>
          
          <p class="text-white">
            <span class="font-semibold">LinkedIn:</span> 
            <a href="https://linkedin.com/in/yourprofile" target="_blank" class="text-blue-600 hover:underline">      Nirmal profile</a>
          </p>
        </div>
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
  alert(`Message sent from: ${name.value}, Email: ${email.value}, Message: ${message.value}`);
  name.value = '';
  email.value = '';
  message.value = '';
};
</script>

<style scoped>
/* Optional custom styles for further refinement */
</style>
