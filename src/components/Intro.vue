<script setup lang="ts">
import { ref, computed, onMounted, onBeforeUnmount } from "vue";

const professions = ["FRONTEND DEVELOPER", "UI/UX DESIGNER", "WEB DEVELOPER"];

const currentIndex = ref(0);
const currentProfession = computed(() => professions[currentIndex.value]);

let intervalId: number | undefined;

onMounted(() => {
  intervalId = setInterval(() => {
    currentIndex.value = (currentIndex.value + 1) % professions.length;
  }, 2000);
});

onBeforeUnmount(() => {
  clearInterval(intervalId);
});

function openLink(url: string) {
  window.open(url, "_blank", "noopener,noreferrer");
}

type Link = {
  name: string;
  url: string;
};

const links: Link[] = [
  {
    name: "Download CV",
    url: "/Temitayo Adebayo_Resume (1).pdf",
  },
  {
    name: "GitHub Link",
    url: "https://github.com/Theezigner"
  },
]
</script>

<template>
  <main
    class="flex flex-col gap-5 md:gap-10 md:flex-row md:justify-between justify-center items-center lg:items-start w-full"
  >
    <div
      class="flex flex-col gap-3 order-2 md:order-1 leading-snug items-center text-center md:text-left md:items-start"
    >
      <div class="text-3xl md:text-5xl lg:text-6xl font-bold  leading-snug">
        <p>Hello, I'm Temitayo ADEBAYO (Theezigner)</p>
        <transition name="slide-up" mode="out-in">
          <p
            :key="currentProfession"
            class="inline-block bg-gradient-to-r from-red-500 to-red-900 bg-clip-text text-transparent lg:text-5xl md:text-4xl text-3xl mt-5"
          >
            {{ currentProfession }}
          </p>
        </transition>
      </div>
      <div
        class="flex flex-row gap-2 mt-5 order-3 text-white font-semibold md:text-lg text-sm leading-normal"
      >
        <button
          v-for="(link, index) in links"
          :key="index"
          @click="openLink(link.url)"
          class="rounded-xl md:rounded-full bg-gradient-to-r from-red-500 to-red-900 py-2 px-2"
        >
          {{ link.name }}
        </button>
        <a href="#contactme" class="bg-white rounded-xl md:rounded-full py-2 px-2">
          <div
            class="bg-gradient-to-r from-red-500 to-red-800 bg-clip-text text-transparent"
          >
            Let's Talk
          </div>
        </a>
      </div>
    </div>

    <div
      class="order-1 md:order-2 p-[0.2px] rounded-lg bg-gradient-to-r from-red-500 to-red-900"
    >
      <img
        src="/ChatGPT Image Aug 9, 2025, 11_59_22 AM.png"
        alt="down arrow"
        class="rounded w-50 h-50 md:w-auto md:h-auto border-[4px] border-solid border-transparent"
      />
    </div>
  </main>
</template>

<style scoped>
.slide-up-enter-active,
.slide-up-leave-active {
  transition: all 0.1s ease;
}
.slide-up-enter-from {
  opacity: 0;
  transform: translateY(50%);
}
.slide-up-leave-to {
  opacity: 0;
  transform: translateY(-50%);
}
</style>
