<template>
  <div class="">
    <!-- Hero Section -->
    <section class="">
      <Hero />
    </section>

    <!-- Bride Section -->
    <section class="">
      <TheBride />
    </section>

    <!-- Groom Section -->
    <section class="">
      <TheGroom />
    </section>

    <!-- Our Story Section -->
    <section class="">
      <OurStory />
    </section>

    <!-- Countdown Section -->
    <section class="n">
      <Countdown />
    </section>

    <!-- Event Section -->
    <section class="">
      <Event />
    </section>
  </div>
</template>

<script setup>
import Hero from "~/components/sections/Hero.vue";
import TheBride from "~/components/sections/TheBride.vue";
import TheGroom from "~/components/sections/TheGroom.vue";
import OurStory from "~/components/sections/OurStory.vue";
import Countdown from "~/components/sections/Countdown.vue";
import Event from "~/components/sections/Event.vue";
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
  scroll-snap-align: center;
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

/* Hide scroll bar */
::-webkit-scrollbar {
  display: none;
}
</style>
