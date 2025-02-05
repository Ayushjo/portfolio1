<template>
  <section class="bg-[#FFF9EC] py-20 relative">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center text-[#3D3D3D] mb-16">My Projects</h2>
      
      <div class="space-y-20">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="relative rounded-lg shadow-lg overflow-hidden transform hover:scale-105 transition-transform duration-300"
          :class="index % 2 === 0 ? 'bg-gradient-to-r from-[#87A398] to-[#FFF9EC]' : 'bg-gradient-to-r from-[#FFF9EC] to-[#87A398]'"
        >
          <div class="grid grid-cols-1 lg:grid-cols-2">
         
            <div class="h-64 lg:h-auto">
              <img :src="project.image" :alt="project.title" class="w-full h-full object-cover">
            </div>

            <div class="p-8 flex flex-col justify-center">
              <h3 class="text-2xl font-bold text-[#3D3D3D]">{{ project.title }}</h3>
              <p class="text-[#3D3D3D] mt-4">{{ project.description }}</p>
              <p class="mt-2 text-sm font-medium text-[#578E7E]">Tech Stack: {{ project.techStack }}</p>
              <a :href="project.link" target="_blank" class="mt-6 inline-block bg-[#578E7E] text-white font-medium px-6 py-3 rounded-lg shadow-md transition-transform hover:scale-105">
                View Project
              </a>
            </div>
          </div>
          
         
          <div class="absolute bottom-0 left-0 w-full h-2 bg-gradient-to-r from-[#FFF9EC] to-[#87A398]"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import MealMasterImg from '../assets/MealMaster.png';
import PortfolioImg from '../assets/Portfolio.png';
import TomatoImg from '../assets/Tomato.png';
const projects = [
  {
    title: "MealMaster",
    description: "A food recipe site with advanced search and meal planning features.",
    techStack: "Vue, TailwindCSS, Firebase, vuex",
    image: MealMasterImg,
    link: "https://meal-master-lyart.vercel.app/"
  },
  {
    title: "Portfolio Site",
    description: "My personal portfolio built with Vue, Vite, and TailwindCSS.",
    techStack: "Vue, Vite, TailwindCSS",
    image: PortfolioImg,
    link: "#"
  },
  {
    title: "Mock Food Delivery",
    description: "Mock Restaurant App ",
    techStack: "Tailwind, JS, Bootstrap",
    image: TomatoImg,
    link: "#"
  }
];
</script>

<style scoped>
section {
  overflow: hidden;
}

div[class*="bg-gradient-to-r"] {
  transition: background 0.3s ease;
}

a:hover {
  background: #3D3D3D;
}
</style>

