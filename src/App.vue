<template>
  <div
    class="relative min-h-screen flex items-center
      justify-center bg-gray-900 overflow-hidden"
  >

    <div
      class="grid-background absolute inset-0 p-2 grid
        grid-cols-12 gap-2 transform -skew-y-12 scale-125"
    >
      <!-- row 1 -->
      <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-5 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-1 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>

      <!-- row 2 -->
      <div class="col-span-5 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-3 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>

      <!-- row 3 -->
      <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-5 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-3 bg-gray-800 rounded animate-pulse"></div>

      <!-- row 4 -->
      <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-3 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-7 bg-gray-800 rounded animate-pulse"></div>

      <!-- row 5 -->
      <div class="col-span-3 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-7 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>

      <!-- row 6 -->
      <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>

      <!-- row 7 -->
      <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-7 bg-gray-800 rounded animate-pulse"></div>
      <div class="col-span-1 bg-gray-800 rounded animate-pulse"></div>
    </div>

    <div class="relative p-3">
      <h2 class="text-3xl md:text-6xl text-white text-center font-extrabold">
        Stay Tuned!
        <a href="https://instagram.com/klifonara" target="_">
          <span class="text-yellow-300">KLIFONARA</span>
          <br />
        </a>
        Is Building Something!
      </h2>
    </div>
  </div>
</template>

<script>
import { onMounted } from "@vue/runtime-core";

export default {
  setup() {
    onMounted(() => {
      const gridItems = document.querySelectorAll(".grid-background > div");
      const getRandomInt = (min, max) => {
        return Math.floor(Math.random() * (max - min + 1)) + min;
      };

      gridItems.forEach((item) => {
        const delay = getRandomInt(0, 5);
        const duration = getRandomInt(3, 6);

        item.style.animationDelay = `${delay}s`;
        item.style.animationDuration = `${duration}s`;
      });
    });
  },
};
</script>
