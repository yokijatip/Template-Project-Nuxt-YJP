<template>
  <div class="relative">
    <!-- Background Slideshow untuk sections yang membutuhkan -->
    <BackgroundSlideshow
      v-if="showBackgroundSlideshow"
      :images="backgroundImages"
      :interval="6000"
    />

    <!-- Main Content dengan Scroll Snap -->
    <div class="relative z-10">
      <!-- Scroll container untuk mobile dan desktop -->
      <div
        class="h-screen overflow-y-auto scroll-smooth snap-y snap-mandatory md:snap-x md:snap-mandatory md:flex md:h-screen md:overflow-x-auto"
      >
        <slot />
      </div>
    </div>
  </div>
</template>

<script setup>
import { computed, ref } from "vue";

// Background images untuk slideshow
const backgroundImages = [
  "/images/couple/IMG_3410.jpg",
  "/images/couple/IMG_3414.jpg",
  // Tambahkan lebih banyak gambar sesuai kebutuhan
];

// Reactive state untuk mengontrol background
const showBackgroundSlideshow = ref(true);

// Method untuk mengontrol background slideshow
const toggleBackgroundSlideshow = (show) => {
  showBackgroundSlideshow.value = show;
};

// Expose methods untuk digunakan di pages
defineExpose({
  toggleBackgroundSlideshow,
});
</script>

<style scoped>
/* Custom scrollbar untuk estetika */
::-webkit-scrollbar {
  width: 4px;
  height: 4px;
}

::-webkit-scrollbar-track {
  background: rgba(255, 255, 255, 0.1);
}

::-webkit-scrollbar-thumb {
  background: rgba(255, 255, 255, 0.3);
  border-radius: 2px;
}

::-webkit-scrollbar-thumb:hover {
  background: rgba(255, 255, 255, 0.5);
}
</style>
