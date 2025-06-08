<template>
  <div class="">
    <Hero />
    <TheBride />
    <TheGroom />
    <OurStory />
    <Countdown />
    <Event />
    <Gallery />
  </div>
</template>

<script setup>
import Hero from "~/components/sections/Hero.vue";
import TheBride from "~/components/sections/TheBride.vue";
import TheGroom from "~/components/sections/TheGroom.vue";
import OurStory from "~/components/sections/OurStory.vue";
import Countdown from "~/components/sections/Countdown.vue";
import Event from "~/components/sections/Event.vue";
import Gallery from "~/components/sections/Gallery.vue";
</script>

<style>
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
