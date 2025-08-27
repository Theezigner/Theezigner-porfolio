<script setup lang="ts">
import HeaderLinks from "./HeaderLinks.vue";
import Hamburger from "./Hamburger.vue";
</script>

<template>
  <main
    class="fixed top-0 left-0 right-0 z-50 shadow-md flex flex-row justify-between items-center py-5 px-5 md:py-8 md:px-20 bg-[#0D0C21]"
  >
    <div class="flex flex-col text-2xl font-bold md:text-4xl">
      <p
        class="bg-gradient-to-r from-red-500 to-red-800 bg-clip-text text-transparent"
      >
        THEEZIGNER
      </p>
      <!-- <p class="bg-gradient-to-r from-red-500 to-red-900 bg-clip-text text-transparent">PORTFOLIO</p> -->
    </div>

    <ul className="flex flex-row gap-8 items-center text-sm text-white-500">
        <HeaderLinks />
        <div className="items-center gap-4">
          <Hamburger />
        </div>
      </ul>
  </main>
</template>

<style scoped></style>
