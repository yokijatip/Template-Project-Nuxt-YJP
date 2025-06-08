<template>
  <div class="fixed inset-0 -z-10">
    <!-- Background Images Slideshow -->
    <div class="relative w-full h-full overflow-hidden">
      <div
        v-for="(image, index) in backgroundImages"
        :key="index"
        :class="[
          'absolute inset-0 transition-opacity duration-1000 ease-in-out',
          currentImageIndex === index ? 'opacity-100' : 'opacity-0',
        ]"
      >
        <NuxtImg
          :src="image"
          :alt="`Background ${index + 1}`"
          class="w-full h-full object-cover"
          loading="eager"
          :preload="index === 0"
        />
        <!-- Overlay untuk readability -->
        <div class="absolute inset-0 bg-black bg-opacity-20"></div>
      </div>
    </div>

    <!-- Gradient overlay untuk transisi yang smooth -->
    <div
      class="absolute inset-0 bg-gradient-to-b from-transparent via-transparent to-black to-opacity-10"
    ></div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted, computed } from "vue";

// Props untuk kontrol slideshow
const props = defineProps({
  images: {
    type: Array,
    default: () => [
      "/images/couple/IMG_3410.jpg",
      "/images/couple/IMG_3414.jpg",
      // Tambahkan gambar lainnya
    ],
  },
  interval: {
    type: Number,
    default: 5000, // 5 detik
  },
  autoPlay: {
    type: Boolean,
    default: true,
  },
});

const currentImageIndex = ref(0);
let slideInterval = null;

const backgroundImages = computed(() => props.images);

const nextImage = () => {
  currentImageIndex.value =
    (currentImageIndex.value + 1) % backgroundImages.value.length;
};

const startSlideshow = () => {
  if (props.autoPlay && backgroundImages.value.length > 1) {
    slideInterval = setInterval(nextImage, props.interval);
  }
};

const stopSlideshow = () => {
  if (slideInterval) {
    clearInterval(slideInterval);
    slideInterval = null;
  }
};

onMounted(() => {
  startSlideshow();
});

onUnmounted(() => {
  stopSlideshow();
});

// Expose methods untuk kontrol external
defineExpose({
  nextImage,
  startSlideshow,
  stopSlideshow,
  currentIndex: currentImageIndex,
});
</script>
