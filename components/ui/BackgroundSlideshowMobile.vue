<template>
  <!-- Background slideshow only visible on mobile -->
  <div
    class="block md:hidden fixed top-0 left-0 w-full h-full -z-10 bg-cover bg-center transition-all duration-7000 shadow-[inset_0_0_0_2000px_rgba(0,0,0,0.5)]"
    :style="`background-image: url(${currentImage})`"
  ></div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const images = ["/img/hero1.jpg", "/img/hero2.jpg", "/img/hero3.jpg"];

const currentImage = ref(images[0]);
let index = 0;

onMounted(() => {
  setInterval(() => {
    index = (index + 1) % images.length;
    currentImage.value = images[index];
  }, 7000);
});
</script>
