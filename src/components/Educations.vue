<script setup lang="ts">
type Educations = {
  name: string;
  years: { start: string; end: string | "Present" };
  description: string;
};

const educations: Educations[] = [
  {
    name: "Altschool Africa",
    years: { start: "2024", end: "25" },
    description:
      "Gained hands-on experience in building modern, responsive, and scalable web applications. Learned and applied HTML, CSS, JavaScript, TypeScript, React, Vite, and Vue, along with best practices in UI/UX, performance optimization, and component-based development. Strengthened problem-solving skills through real-world projects, teamwork, and continuous learning in a fast-paced environment.",
  },
  {
    name: "Scrimba",
    years: { start: "2025", end: "Present" },
    description:
      "Completed an immersive, project-based program focused on Next.js, JavaScript, TypeScript, and React. Built interactive web applications while strengthening problem-solving skills, state management, and modern frontend workflows. Gained practical experience through coding challenges and hands-on projects that emphasized clean, reusable code and responsive design.",
  },
  {
    name: "Vue Mastery",
    years: { start: "2025", end: "Present" },
    description:
      "Focused on mastering Vue.js through structured tutorials and hands-on practice. Learned key concepts such as the Composition API, component-based architecture, reactivity, and state management. Applied these lessons by building interactive projects, reinforcing best practices for writing clean, maintainable Vue code.",
  },
  {
    name: "Zuri x Ingressive",
    years: { start: "2022", end: "22" },
    description:
      "Participated in an intensive training program focused on UI/UX design fundamentals. Gained practical experience in user research, wireframing, prototyping, and visual design while collaborating with peers on real-world projects. Built a strong foundation in creating user-centered digital experiences with attention to accessibility and aesthetics.",
  },
  {
    name: "Coursera",
    years: { start: "2022", end: "22" },
    description:
      "Completed a professional course in UI/UX Design, gaining a strong foundation in user research, wireframing, prototyping, and usability principles. Learned how to design intuitive and user-centered interfaces while applying industry-standard tools and design thinking methods to real-world projects.",
  },
  {
    name: "Canva 4 E",
    years: { start: "2021", end: "21" },
    description:
      "Completed training in graphic design principles including color theory, typography, layout, and visual storytelling. Learned to create engaging digital assets such as social media graphics, presentations, and branding materials using Canva’s design tools. Built a strong foundation in visual communication and creative problem-solving.",
  },
];
</script>

<template>
  <main
    id="education"
    class="w-full flex flex-col items-center justify-center text-center md:items-start md:text-left"
  >
    <h2 class="font-bold text-4xl md:text-5xl">Educations</h2>

    <section
      class="flex flex-col justify-between gap-10  mt-10 md:w-full"
    >
      <div v-for="(education, index) in educations" :key="index" class="">
        <div class="flex flex-row md:gap-5 gap-3 mb-5 items-center">
            <div class="md:w-8 md:h-8 w-5 h-5 rounded-full bg-gradient-to-r from-red-500 to-red-900 mr-5"></div>
          <p class="text-xl md:text-4xl font-semibold text-left">{{ education.name }}</p>
          <div class="rounded-lg bg-gradient-to-r from-red-500 to-red-900 py-1 px-3 md:text-2xl text-white font-semibold text-center ">
            <p>{{ education.years.start }} - {{ education.years.end }}</p>
          </div>
        </div>
        <div
          class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-auto h-full ml-18 "
        >
          <div
            class="flex flex-col rounded-lg w-auto h-full bg-[#0D0C21] flex items-start text-white px-4 md:p-5"
          >
            <p class="md:text-justify text-sm md:text-xl font-normal text-gray-300 my-3">
              {{ education.description }}
            </p>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>


