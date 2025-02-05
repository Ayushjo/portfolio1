<template>
  <section class="bg-[#578E7E] py-20">
    <div class="container mx-auto px-6 text-center text-white">
      <h2 class="text-4xl font-bold mb-6">Let’s Get In Touch</h2>
      <p class="text-lg md:text-xl mb-8">
        Whether you have a project in mind or just want to chat, I'm always open to exciting opportunities!
      </p>
      
      
      <div class="flex justify-center gap-12 mb-12">
        <!-- Email -->
        <a href="mailto:your-ayushs24101@iiitnr.edu.in" class="flex items-center space-x-2 hover:text-[#FFF9EC] transition-all duration-300 transform hover:scale-105">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-8 h-8">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 7l9 6 9-6"></path>
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 7v10l9 6 9-6V7"></path>
          </svg>
          <span class="text-lg font-semibold">Email</span>
        </a>

     
        <a href="https://www.linkedin.com/in/your-profile" target="_blank" class="flex items-center space-x-2 hover:text-[#FFF9EC] transition-all duration-300 transform hover:scale-105">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-8 h-8">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 8a6 6 0 11-12 0 6 6 0 0112 0zM3 12v8h4v-8H3zm14 0v8h4v-8h-4z"></path>
          </svg>
          <span class="text-lg font-semibold">LinkedIn</span>
        </a>

      
        <a href="https://github.com/Ayushjo" target="_blank" class="flex items-center space-x-2 hover:text-[#FFF9EC] transition-all duration-300 transform hover:scale-105">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="w-8 h-8">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 2C6.48 2 2 6.48 2 12c0 4.41 3.29 8.08 7.73 9.39.56.1.76-.24.76-.51 0-.27-.01-1.03-.01-2.02-3.14.68-3.8-1.52-3.8-1.52-.51-1.29-1.24-1.63-1.24-1.63-.99-.68.07-.67.07-.67 1.09.08 1.66 1.13 1.66 1.13 1.03 1.77 2.71 1.26 3.36.97.1-.74.4-1.26.73-1.56-2.28-.26-4.66-1.14-4.66-5.08 0-1.12.4-2.04 1.06-2.76-.11-.26-.46-1.3.1-2.72 0 0 .85-.27 2.77 1.02a9.674 9.674 0 014.93 0c1.91-1.3 2.77-1.02 2.77-1.02.57 1.42.21 2.46.1 2.72.66.72 1.06 1.64 1.06 2.76 0 3.94-2.38 4.82-4.66 5.08.42.36.81 1.07.81 2.15 0 1.55-.01 2.8-.01 3.19 0 .28.2.61.76.51A9.96 9.96 0 0022 12c0-5.52-4.48-10-10-10z"></path>
          </svg>
          <span class="text-lg font-semibold">GitHub</span>
        </a>
      </div>

      
      <form action="#" method="POST" class="max-w-lg mx-auto space-y-6 bg-white p-8 rounded-lg shadow-lg">
        <div class="flex flex-col space-y-4">
          <input
            type="text"
            name="name"
            placeholder="Your Name"
            class="p-4 rounded-md text-[#3D3D3D] border-2 border-[#578E7E] focus:outline-none focus:ring-2 focus:ring-[#578E7E] transition-all"
          />
          <input
            type="email"
            name="email"
            placeholder="Your Email"
            class="p-4 rounded-md text-[#3D3D3D] border-2 border-[#578E7E] focus:outline-none focus:ring-2 focus:ring-[#578E7E] transition-all"
          />
          <textarea
            name="message"
            placeholder="Your Message"
            rows="4"
            class="p-4 rounded-md text-[#3D3D3D] border-2 border-[#578E7E] focus:outline-none focus:ring-2 focus:ring-[#578E7E] transition-all"
          ></textarea>
        </div>
        <button
        type="button"
          
          class="bg-[#578E7E] text-white p-4 rounded-md hover:bg-[#3D3D3D] transition-all duration-300 transform hover:scale-105 w-full"
          @click="show=true"
        >
          Send Message
        </button>
        <p v-if="show===true" class="text-lg md:text-xl mb-8 text-black">Message Sent</p>
      </form>
    </div>
  </section>
</template>

<script setup>
import {ref} from 'vue'
const show = ref(false)


 
</script>

<style scoped>
 
  input, textarea {
    transition: all 0.3s ease;
  }
  input:focus, textarea:focus {
    box-shadow: 0 0 5px 2px rgba(87, 142, 126, 0.5);
  }
</style>
