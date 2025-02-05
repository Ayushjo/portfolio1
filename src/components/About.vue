<template>
  <section class="bg-[#F5ECD5] py-20">
    <div class="container mx-auto px-6">
      <h2 class="text-4xl font-bold text-center text-[#3D3D3D] mb-16">My Journey</h2>
      <div class="relative border-l-4 border-[#578E7E]">
        <div v-for="(event, index) in timeline" :key="index" class="mb-10 ml-6">
         
          <div class="absolute w-4 h-4 bg-[#578E7E] rounded-full -left-2 top-0"></div>
          
         
          <div class="bg-[#FFF9EC] p-6 rounded-lg shadow-lg">
            <h3 class="text-2xl font-semibold text-[#3D3D3D]">{{ event.title }}</h3>
            <p class="text-sm text-[#3D3D3D] mt-1">{{ event.date }}</p>
            <p class="mt-4 text-[#3D3D3D]">{{ event.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const timeline = [
  {
    title: "Started My Coding Journey",
    date: "2024",
    description: "Began learning HTML, CSS, and JavaScript. Built small projects and fell in love with web development."
  },
  {
    title: "Discovered Vue & React",
    date: "2025",
    description: "Started building more advanced projects with Vue and React. Created MealMaster and my portfolio site."
  },
  {
    title: "Exploring AI & Machine Learning",
    date: "2025",
    description: "Became interested in AI/ML and started learning about neural networks and data science."
  },
  {
    title: "Future Goals",
    date: "2026 & Beyond",
    description: "Aim to work on innovative projects that blend web development with AI/ML for real-world impact."
  }
];
</script>

<style scoped>
section {
  overflow: hidden;
}
</style>

