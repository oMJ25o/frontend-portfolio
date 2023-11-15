<template>
  <div class="container-all" id="container-all">
    <Navbar />
    <Profile />
    <About />
    <Skills />
    <Contact />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Profile from './components/Profile.vue'
import About from './components/About.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
</script>

<style>
body {
  width: 100%;
  margin: 0;
  font-family: 'Exo', sans-serif;
}

.container-all {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.container-arrow {
  justify-content: center;
}

#arrow-pic {
  width: fit-content;
  height: 3vh;
}
</style>
