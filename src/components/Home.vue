<template>
  <div class="scroll-smooth">
    <section id="Home" class="bg-[#F5ECD5] min-h-screen flex items-center justify-center relative">
      <div class="container mx-auto px-6 text-center">
        
        <h1 class="text-4xl md:text-6xl font-bold text-[#3D3D3D] leading-tight font-poppins">
          <span ref="typingText"></span><span class="typed-cursor">|</span>
        </h1>

        
        <p class="mt-4 text-lg md:text-xl text-[#3D3D3D] font-poppins">
          Let’s create something amazing together.
        </p>

       
        <div class="mt-8 flex justify-center space-x-4">
          <a href="#Projects" class="bg-[#578E7E] text-[#FFF9EC] font-medium py-3 px-6 rounded-lg hover:bg-[#3D3D3D] transition-colors font-poppins">
            View My Work
          </a>
          <a href="#Contact" class="border border-[#578E7E] text-[#3D3D3D] font-medium py-3 px-6 rounded-lg hover:bg-[#578E7E] hover:text-[#FFF9EC] transition-colors font-poppins">
            Contact Me
          </a>
        </div>

      
        <div class="absolute bottom-4 left-1/2 transform -translate-x-1/2 animate-bounce">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="40" height="40" class="text-[#3D3D3D]">
            <path d="M12 2v16m-7-7l7 7 7-7" stroke="#3D3D3D" stroke-width="2" fill="none" />
          </svg>
        </div>
      </div>
    </section>

    <About id="About" />
    <FeaturedSkills id="Skills" />
    <PortfolioSection id="Projects" />
    <Testimonials id="Testimonials" />
    <Contact id="Contact" />
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import About from "./About.vue";
import FeaturedSkills from "./FeaturedSkills.vue";
import PortfolioSection from "./PortfolioSection.vue";
import Testimonials from "./Testimonials.vue";
import Contact from "./Contact.vue";

const typingText = ref(null);
const messages = ["Hi, I am Ayush.", "A Passionate Developer.", "Focused on Building Clean Web Experiences."];
let messageIndex = 0;
let charIndex = 0;
const typingSpeed = 100;

const typeEffect = () => {
  if (messageIndex < messages.length) {
    const currentMessage = messages[messageIndex];
    if (charIndex < currentMessage.length) {
      typingText.value.innerHTML += currentMessage[charIndex];
      charIndex++;
      setTimeout(typeEffect, typingSpeed);
    } else {
      charIndex = 0;
      messageIndex++;
      setTimeout(() => {
        typingText.value.innerHTML = "";
        typeEffect();
      }, 1500);
    }
  } else {
    messageIndex = 0;
    setTimeout(typeEffect, 500);
  }
};

onMounted(() => {
  typeEffect();
  
  
});

</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap");

.font-poppins {
  font-family: "Poppins", sans-serif;
}

.typed-cursor {
  font-weight: bold;
  color: #3d3d3d;
  animation: blink 1s step-end infinite;
}

@keyframes blink {
  50% {
    opacity: 0;
  }
}
</style>

