<template>
  <section class="bg-[#FFF9EC] py-20 ">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-3xl font-bold text-[#3D3D3D] mb-16 font-poppins">My Skills</h2>
      
     
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-12">
       
        <div class="skill-card text-center">
          <img
            src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/html5.svg"
            alt="HTML"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">HTML</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: htmlProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>

      
        <div class="skill-card text-center">
          <img
            src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/css3.svg"
            alt="CSS"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">CSS</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: cssProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>

       
        <div class="skill-card text-center">
          <img
            src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/javascript.svg"
            alt="JavaScript"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">JavaScript</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: jsProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>

  
        <div class="skill-card text-center">
          <img
            src="../images/icons8-vue-js-48.png"
            alt="Vue"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">Vue.js</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: vueProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>

    
        <div class="skill-card text-center">
          <img
            src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/react.svg"
            alt="React"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">React</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: reactProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>

        <div class="skill-card text-center">
          <img
            src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/vite.svg"
            alt="Vite"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">Vite</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: viteProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>


        <div class="skill-card text-center">
          <img
            src="../images/Next.js.png"
            alt="Next.js"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">Next.js</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: nextjsProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>

   
        <div class="skill-card text-center">
          <img
            src="../assets/node-js-black-icon.png"
            alt="Node.js"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">Node.js</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: nodejsProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>

        <div class="skill-card text-center">
          <img
            src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/express.svg"
            alt="Express"
            class="mx-auto mb-4 w-16 h-16"
          />
          <h3 class="text-xl font-semibold text-[#3D3D3D]">Express</h3>
          <div
            class="progress-bar bg-[#578E7E] mt-4 rounded-lg h-4"
            :style="{ width: expressProgress + '%' }"
            v-bind:class="{ 'animate-progress': isVisible }"
          ></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const isVisible = ref(false);


const htmlProgress = ref(0);
const cssProgress = ref(0);
const jsProgress = ref(0);
const vueProgress = ref(0);
const reactProgress = ref(0);
const viteProgress = ref(0);
const nextjsProgress = ref(0);
const nodejsProgress = ref(0);
const expressProgress = ref(0);

onMounted(() => {
  setTimeout(() => {
   
    htmlProgress.value = 90;
    cssProgress.value = 75;
    jsProgress.value = 80;
    vueProgress.value = 90;
    reactProgress.value = 40;
    viteProgress.value = 90;
    nextjsProgress.value = 10;
    nodejsProgress.value = 15;
    expressProgress.value = 15;

    isVisible.value = true;
  }, 100); 
});
</script>

<style scoped>
.skill-card {
  transition: transform 0.3s ease-in-out;
}

.skill-card:hover {
  transform: translateY(-10px); 
}

.progress-bar {
  width: 0; 
  transition: width 2s ease-out; 
}

.animate-progress {
  width: inherit;
}
</style>


