<template>
  <section class="relative py-20 bg-gradient-to-br from-[#FFF9EC] to-[#F5ECD5] overflow-hidden">
    
    <div class="absolute -top-10 -left-10 w-32 h-32 bg-[#578E7E] rounded-full opacity-20 animate-float"></div>
    <div class="absolute -bottom-10 -right-16 w-48 h-48 bg-[#3D3D3D] rounded-full opacity-30 animate-pulse"></div>
    
    <div class="container mx-auto px-6 text-center relative z-10">
      <h2 class="text-3xl font-bold text-[#3D3D3D] mb-8">What People Think</h2>
      <p class="text-lg text-[#578E7E] mb-12">
        Here’s what some awesome people have said about collaborating with me.
      </p>

     
      <div class="swiper-container">
        <div class="swiper-wrapper">
        
          <div class="swiper-slide bg-white p-8 shadow-lg rounded-xl">
            <p class="text-lg italic text-[#3D3D3D]">
              “Working with you has been a game-changer! Your attention to detail and creative solutions always exceed expectations.”
            </p>
            <h4 class="mt-6 font-semibold text-[#578E7E]">- Alex Johnson, Developer</h4>
          </div>

        
          <div class="swiper-slide bg-white p-8 shadow-lg rounded-xl">
            <p class="text-lg italic text-[#3D3D3D]">
              “Your ability to turn ideas into reality is incredible. Looking forward to our next project together!”
            </p>
            <h4 class="mt-6 font-semibold text-[#578E7E]">- Sarah Williams, Designer</h4>
          </div>

        
          <div class="swiper-slide bg-white p-8 shadow-lg rounded-xl">
            <p class="text-lg italic text-[#3D3D3D]">
              “A fantastic experience! You’re a true professional with great insights and creative vision.”
            </p>
            <h4 class="mt-6 font-semibold text-[#578E7E]">- Michael Lee, Project Manager</h4>
          </div>
        </div>
      
        <div class="swiper-pagination mt-6"></div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue';
import Swiper from 'swiper/bundle';
import 'swiper/swiper-bundle.css';


onMounted(() => {
  new Swiper('.swiper-container', {
    loop: true,
    autoplay: {
      delay: 3000,
    },
    pagination: {
      el: '.swiper-pagination',
      clickable: true,
    },
  });
});
</script>

<style scoped>
/* Floating animation */
@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(20px);
  }
  100% {
    transform: translateY(0px);
  }
}

.animate-float {
  animation: float 6s infinite;
}

.animate-pulse {
  animation: pulse 8s infinite;
}

.swiper-slide {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>

