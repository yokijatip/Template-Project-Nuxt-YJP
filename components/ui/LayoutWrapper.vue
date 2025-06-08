<template>
  <div class="relative h-screen w-screen overflow-hidden">
    <!-- Fixed Image for Desktop Only -->
    <div
      class="hidden md:block w-1/2 h-full fixed top-0 left-0 bg-cover bg-center"
      style="background-image: url('/img/hero1.jpg')"
    ></div>

    <!-- Background Slideshow for Mobile Only -->
    <BackgroundSlideshowMobile />

    <!-- Scrollable Content on Right -->
    <div
      class="w-full md:w-1/2 md:ml-auto h-screen overflow-y-scroll snap-y snap-mandatory"
    >
      <NuxtPage />
    </div>
  </div>
</template>

<script setup>
import BackgroundSlideshowMobile from "~/components/ui/BackgroundSlideshowMobile.vue";
</script>

<style scoped>
html,
body {
  overflow: hidden;
  margin: 0;
  padding: 0;
}
</style>
