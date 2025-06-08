<template>
  <div class="min-h-screen bb br">
    <!-- Container Content -->
    <section class="flex items-center justify-center min-h-screen p-5">
      <!-- Content -->
      <!-- Use Glass Effect use tailwind blur -->
      <div
        class="flex flex-col items-center justify-center br px-5 py-10 gap-10"
      >
        <!-- Akad -->
        <div class="flex flex-col gap-1">
          <h1 class="font-serif text-3xl uppercase font-semibold text-white">
            akad
          </h1>
          <h2 class="font-serif uppercase font-semibold text-primary-white">
            minggu, 8 juni 2025
          </h2>
          <h3 class="text-xs font-sans tracking-wider text-primary-white">
            08.00 - 09.00 WIB
          </h3>
          <h2 class="font-serif uppercase font-semibold text-white">
            kediaman mempelai wanita
          </h2>
          <p
            class="text-xs font-sans tracking-wider font-thin text-primary-white"
          >
            Kp. Sukamaju 03/09 Desa Sarimukti, Kec. Cipatat, Kab.Bandung Barat
          </p>
          <!-- Button Lihat Lokasi and Open Google Maps Use Nuxt UI Button, button with text Lihat Lokasi and Arrow icon, and then the bg button is transparent but have a border with 1 or 2 px and color white  -->
          <!-- Tombol Lihat Lokasi -->
          <button
            class="mt-4 uppercase text-xs font-semibold text-white border border-white hover:bg-white/10 transition-all duration-300 w-fit py-2 px-4"
            @click="openMap('akad')"
          >
            <span>Lihat Lokasi</span>
            <NuxtIcon name="heroicons-outline:arrow-right" class="w-5 h-5" />
          </button>
        </div>

        <div class="flex flex-col gap-1">
          <h1 class="font-serif text-3xl uppercase font-semibold text-white">
            Resepsi
          </h1>
          <h2 class="font-serif uppercase font-semibold text-primary-white">
            minggu, 8 juni 2025
          </h2>
          <h3 class="text-xs font-sans tracking-wider text-primary-white">
            08.00 - 09.00 WIB
          </h3>
          <h2 class="font-serif uppercase font-semibold text-white">
            kediaman mempelai wanita
          </h2>
          <p
            class="text-xs font-sans tracking-wider font-thin text-primary-white"
          >
            Kp. Sukamaju 03/09 Desa Sarimukti, Kec. Cipatat, Kab.Bandung Barat
          </p>
          <!-- Button Lihat Lokasi and Open Google Maps Use Nuxt UI Button, button with text Lihat Lokasi and Arrow icon, and then the bg button is transparent but have a border with 1 or 2 px and color white  -->
          <button
            class="mt-4 uppercase text-xs font-semibold text-white border border-white hover:bg-white/10 transition-all duration-300 w-fit py-2 px-4"
            @click="openMap('akad')"
          >
            <span>Lihat Lokasi</span>
            <NuxtIcon name="heroicons-outline:arrow-right" class="w-5 h-5" />
          </button>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const openMap = (type) => {
  const locationUrl =
    "https://maps.google.com/?q=Kp.+Sukamaju+03%2F09+Desa+Sarimukti,+Kec.+Cipatat,+Kab.+Bandung+Barat";
  window.open(locationUrl, "_blank");
};
</script>

<style scoped>
/* Border Line */
.br {
  border: 1px solid red;
}

.bb {
  border: 1px solid blue;
}

.bgr {
  border: 1px solid green;
}

.bw {
  border: 1px solid white;
}

.by {
  border: 1px solid yellow;
}
</style>
