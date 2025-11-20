<script setup lang="ts">
import { ref } from "vue";

const isOpen = ref(false);

function hamburger() {
  isOpen.value = !isOpen.value;
  return isOpen;
}
</script>

<template>
  <main class="md:hidden cursor-pointer">
    <button
      @click="hamburger"
      class="space-y-1 w-4 h-4 grid place-items-center rounded relative z-50"
    >
      <span
        :class="isOpen ? 'rotate-50 translate-y-2' : ''"
        class="block h-0.5 w-full bg-white rounded transform transition duration-300 ease-in-out"
      ></span>
      <span
        :class="isOpen ? 'opacity-0' : 'opacity-100'"
        class="block h-0.5 w-full bg-white rounded transform transition-opacity duration-300 ease-in-out"
      ></span>
      <span
        :class="isOpen ? '-rotate-50 -translate-y-1' : ''"
        class="block h-0.5 w-full bg-white rounded transform transition duration-300 ease-in-out"
      ></span>
    </button>

    <aside class="md:hidden">
      <nav
        v-if="isOpen"
        class="absolute top-16 right-5 left-5 bg-[#0D0C21] border border-gray-800 p-5 rounded shadow-md flex flex-col gap-5"
      >
        <a href="#aboutme">About Me</a>
        <a href="#skills&tools">Skills & Tools</a>
        <a href="#projects">Projects</a>
        <a href="#education">Education</a>
      </nav>
    </aside>
  </main>
</template>

<style scoped></style>
