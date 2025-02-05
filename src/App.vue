<script setup>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
import TypedJs from 'vue-typed-js';

</script>

<template>
<div class="scroll-smooth">
    <Navbar />
    <Home />
    <router-view />
  </div>
</template>

<style scoped>

</style>
