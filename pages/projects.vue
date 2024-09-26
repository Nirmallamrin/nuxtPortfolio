<template>
    <div class="bg-gray-100 p-8">
      <h1 class="font-bold italic text-gray-900 text-5xl flex justify-center mb-12">My Projects</h1>
      <div class="container mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div v-for="(project, index) in projects" :key="index" class="bg-white p-6 rounded-lg shadow-lg transition-transform transform hover:scale-105">
            <img :src="project.imageUrl" :alt="project.title" class="w-full h-40 object-cover rounded-t-lg" />
            <div class="mt-4">
              <h2 class="text-xl font-semibold mb-2">{{ project.title }}</h2>
              <p class="text-gray-700 mb-4">{{ project.description }}</p>
              <a :href="project.liveLink" class="text-blue-500 hover:underline mr-4" target="_blank" rel="noopener noreferrer">Live Page</a>
              <a :href="project.githubLink" class="text-blue-500 hover:underline" target="_blank" rel="noopener noreferrer">GitHub</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import ecommerce from '@/public/IMG39.jpg';
  import news from '@/public/IMG40.jpg';
  import weather from '@/public/IMG41.png';
  import todo from '@/public/IMG42.png';
  import expense from '@/public/IMG43.png';
  
  // Project data
  const projects = ref([
    {
      title: 'E-Commerce Web Application',
      description: 'A full-featured e-commerce web application built using the MERN stack.',
      imageUrl: news,
      liveLink: 'https://e-commerce-fe-cyan.vercel.app/',
      githubLink: 'https://github.com/Nirmallamrin',
    },
    {
      title: 'News Website',
      description: 'A news website that aggregates articles from various sources, using MERN Stack.',
      imageUrl: ecommerce,
      liveLink: 'https://entri-news-client.vercel.app/',
      githubLink: 'https://github.com/Nirmallamrin',
    },
    {
      title: 'Weather App',
      description: 'Weather App using React Vite.',
      imageUrl: weather,
      liveLink: 'https://weather-app-dun-kappa-84.vercel.app/',
      githubLink: 'https://github.com/Nirmallamrin/WeatherApp.git',
    },
    {
      title: 'To Do List',
      description: 'To Do List App using React Vite.',
      imageUrl: todo,
      liveLink: 'https://to-do-list-seven-beta-43.vercel.app/',
      githubLink: 'https://github.com/Nirmallamrin/To-Do-List.git',
    },
    {
      title: 'Expense Tracker',
      description: 'Expense Tracker App using React Vite.',
      imageUrl: expense,
      liveLink: 'https://expense-tracker-rouge-ten.vercel.app/',
      githubLink: 'https://github.com/Nirmallamrin/ExpenseTracker.git',
    },
  ]);
  </script>
  
  <style scoped>
  </style>
  