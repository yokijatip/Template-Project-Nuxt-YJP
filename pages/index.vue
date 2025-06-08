<template>
  <div class="scroll-container">
    <!-- Hero Section -->
    <section class="snap-section">
      <Hero />
    </section>

    <!-- Bride Section -->
    <section class="snap-section">
      <TheBride />
    </section>

    <!-- Groom Section -->
    <section class="snap-section">
      <TheGroom />
    </section>

    <!-- Our Story Section -->
    <section class="snap-section">
      <OurStory />
    </section>
  </div>
</template>

<script setup>
import Hero from "~/components/sections/Hero.vue";
import TheBride from "~/components/sections/TheBride.vue";
import TheGroom from "~/components/sections/TheGroom.vue";
import OurStory from "~/components/sections/OurStory.vue";
</script>

<style scoped>
.scroll-container {
  height: 100vh;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
}

.snap-section {
  height: 100vh;
  scroll-snap-align: start;
  scroll-snap-stop: always;
}

.br {
  border: 1px solid red;
}

.bb {
  border: 1px solid blue;
}

.by {
  border: 1px solid yellow;
}

.bw {
  border: 1px solid white;
}
</style>
