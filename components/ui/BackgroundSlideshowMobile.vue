<template>
  <!-- Background slideshow only visible on mobile -->
  <div
    class="blockmd: fixed top-0 left-0 w-full h-full -z-10 bg-cover bg-center transition-all duration-7000 shadow-[inset_0_0_0_2000px_rgba(0,0,0,0.5)]"
    :style="`background-image: url(${currentImage})`"
  ></div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const images = [
  "/img/hero1.jpg",
  "/img/hero3.jpg",
  "/img/gallery1.jpg",
  "/img/gallery2.jpg",
  "/img/gallery3.jpg",
  "/img/gallery4.jpg",
  "/img/gallery5.jpg",
  "/img/gallery6.jpg",
  "/img/gallery7.jpg",
  "/img/gallery8.jpg",
  "/img/gallery9.jpg",
  "/img/gallery10.jpg",
  "/img/gallery11.jpg",
  "/img/ourstory1.jpg",
  "/img/ourstory2.jpg",
  "/img/ourstory3.jpg",
];

const currentImage = ref(images[0]);
let index = 0;

onMounted(() => {
  setInterval(() => {
    index = (index + 1) % images.length;
    currentImage.value = images[index];
  }, 7000);
});
</script>

<style scoped>
/* Hide scroll bar */
::-webkit-scrollbar {
  display: none;
}
</style>
