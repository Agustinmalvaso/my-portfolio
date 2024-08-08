<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import About from "./components/About.vue";
import Carousel from "./components/Skills.vue";
</script>

<template>
  <div class="app">
    <Navbar />
    <div class="slides slide1 flex flex-row gap-0 justify-center">
      <About />
    </div>
    <div class="slides slide2">
      <Carousel />
    </div>
    <div class="slides slide3">
      <h1>SECTION 3</h1>
    </div>
  </div>
</template>

<style scoped>
.app {
  margin: 0;
  padding: 0;
  height: 100vh;
  width: 100%;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
  box-sizing: border-box;
}

.slides {
  height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  scroll-snap-align: start;
  box-sizing: border-box;
}

.slides h1 {
  font-size: 70px;
  font-weight: 600;
  color: #fff;
}

.slide1 {
  background: linear-gradient(454deg, #3c0dd8, #202329);
}
.slide2 {
  background: linear-gradient(454deg, #404c80, #53ff88);
}
.slide3 {
  background: linear-gradient(454deg, #9574ff, #ff5353);
}
</style>
