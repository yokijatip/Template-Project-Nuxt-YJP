<template>
  <div>
    <!-- Set the overlay shadow for image background -->
    <section
      class="bg-[url(@/assets/images/gallery/IMG_3379.jpg)] bg-cover bg-center bg-no-repeat shadow-[inset_0_0_0_2000px_rgba(0,0,0,0.5)]"
    >
      <!-- Content -->
      <div
        class="container mx-auto flex flex-col items-center justify-between min-h-screen text-primary-white"
      >
        <!-- Top Content -->
        <div
          class="flex flex-row items-center gap-2 justify-between w-full p-12 text-xs/4 md:text-md font-bold font-sans mt-12 text-center"
        >
          <!-- Day -->
          <p>
            HARI <br />
            MINGGU
          </p>

          <!-- Date -->
          <p>
            BULAN <br />
            08 JUN
          </p>

          <!-- Year -->
          <p>
            TAHUN <br />
            2025
          </p>
        </div>

        <!-- Bottom Content -->
        <div class="flex flex-col items-center gap-5 p-10 mb-32">
          <h2 class="text-2xl font-cursive">The Wedding Of</h2>
          <h1 class="text-4xl font-serif">Ghani & Wiwit</h1>
          <p class="text-center text-xs font-sans md:w-1/2">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto,
            dolores! Ad nulla odio voluptas quidem? Cupiditate fugiat
            dignissimos ratione odio ducimus voluptas eligendi cum.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup></script>

<style></style>
