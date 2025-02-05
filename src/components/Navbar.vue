<template>
  <nav class="fixed top-0 left-0 w-full bg-white/30 backdrop-blur-md z-50">
    <div class="container mx-auto flex items-center justify-between py-4 px-6">
     
      <img src="https://thumbs.dreamstime.com/b/letter-logo-design-simple-modern-logo-design-letter-very-simple-black-background-color-183193944.jpg" class="w-16 h-16 rounded-md" />
        
      

     
      <ul class="hidden md:flex space-x-8">
        <li v-for="(item, index) in menuItems" :key="index">
          <a
            :href="item.link"
            class="text-lg font-medium text-[#3D3D3D] hover:text-[#578E7E] transition-colors"
          >
            {{ item.name }}
          </a>
        </li>
      </ul>

    
      <button class="md:hidden text-2xl text-[#3D3D3D]" @click="toggleMenu">
        ☰
      </button>
    </div>

  
    <transition name="fade">
      <div v-if="showMenu" class="md:hidden bg-white/70 backdrop-blur-md absolute top-full left-0 w-full py-6">
        <ul class="space-y-6 text-center">
          <li v-for="(item, index) in menuItems" :key="index">
            <a
              :href="item.link"
              class="text-lg font-medium text-[#3D3D3D] hover:text-[#578E7E] transition-colors"
              @click="toggleMenu"
            >
              {{ item.name }}
            </a>
          </li>
        </ul>
      </div>
    </transition>
  </nav>
</template>

<script setup>
import { ref } from 'vue';

const menuItems = [
  { name: "Home", link: "#Home" },
  { name: "About", link: "#About" },
  { name: "Skills", link: "#Skills" },
  { name: "Projects", link: "#Projects" },
  {name:"Testimonials",link:"#Testimonials"},
  { name: "Contact", link: "#Contact" }
];

const showMenu = ref(false);

const toggleMenu = () => {
  showMenu.value = !showMenu.value;
};
</script>

<style scoped>
nav {
  transition: all 0.3s ease-in-out;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>

