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
      class="space-y-1 w-4 h-4 grid place-items-center rounded"
    >
      <span className="bg-white block h-0.5 w-5"></span>
      <span className="bg-white block h-0.5 w-5"></span>
      <span className="bg-white block h-0.5 w-5"></span>
    </button>

    <aside class="md:hidden">
      <nav
        v-if="isOpen"
        class="absolute top-16 right-5 bg-gray-800 p-5 rounded shadow-md flex flex-col gap-5"
      >
        <div @click="isOpen = false" class="font-bold pb-1 self-end text-base">
          <p>X</p>
        </div>
        <a href="#aboutme">About Me</a>
        <a href="#skills&tools">Skills & Tools</a>
        <a href="#projects">Projects</a>
        <a href="#education">Education</a>
      </nav>
    </aside>
  </main>
</template>

<style scoped></style>
