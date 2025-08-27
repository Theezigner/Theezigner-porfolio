<script setup lang="ts">
type Skills = {
  image: string;
  name: string;
};
const languages: Skills[] = [
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg",
    name: "HTML5",
  },
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg",
    name: "CSS3",
  },
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
    name: "JavaScript",
  },
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg",
    name: "TypeScript",
  },
];

const frameworks: Skills[] = [
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg",
    name: "Vue.js",
  },
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg",
    name: "React",
  },
  {
    image: "/vite.svg",
    name: "Vite",
  },
  {
    image: "/tailwindcss-mark.d52e9897.svg",
    name: "Tailwind CSS",
  },
];

const designTools: Skills[] = [
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg",
    name: "Figma",
  },
  {
    image: "/Adobe Photoshop en App Store.jpg",
    name: "Photoshop",
  },
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/illustrator/illustrator-plain.svg",
    name: "Illustrator",
  },
  {
    image: "/Canva.jpg",
    name: "Canva",
  },
];

const technologies: Skills[] = [
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
    name: "Git",
  },
  {
    image: "/c927d61a-fcd4-4b3b-85c8-fb7bf436c4aa-removebg-preview.png",
    name: "GitHub",
  },
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/npm/npm-original-wordmark.svg",
    name: "npm",
  },
  {
    image:
      "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg",
    name: "VS Code",
  },
];

const softSkills: string[] = [
  "Effective Communication",
  "Team Collaboration",
  "Debugging",
  "Problem-Solving",
  "Adaptability",
  "Time Management",
];
</script>

<template>
  <main
    id="skills&tools"
    class="w-full flex flex-col items-center justify-center text-center md:items-start md:text-left"
  >
    <h2 class="font-bold text-4xl md:text-5xl">Skills & Tools</h2>

    <section
      class="grid grid-cols-1 md:grid-cols-2 justify-between md:flex-row gap-10 md:gap-10 mt-10 md:w-full md:h-full"
    >
      <div
        class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-full h-full"
      >
        <div
          class="flex flex-col rounded-lg w-full h-full bg-[#0D0C21] flex items-center text-white px-20 md:px-0"
        >
          <p class="text-3xl font-bold mt-2">Languages</p>

          <div class="grid grid-cols-2 gap-20 my-10">
            <div
              v-for="(language, index) in languages"
              :key="index"
              class="flex flex-col items-center"
            >
              <img
                :src="language.image"
                :alt="language.name"
                class="w-20 h-20 mx-5 md:w-20 md:h-20"
              />
              <p class="text-sm mt-2">{{ language.name }}</p>
            </div>
          </div>
        </div>
      </div>

      <div
        class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-full h-full"
      >
        <div
          class="flex flex-col rounded-lg w-full h-full bg-[#0D0C21] flex items-center text-white px-20 md:px-0"
        >
          <p class="text-3xl font-bold mt-2">Frameworks/Build Tools</p>

          <div class="grid grid-cols-2 gap-20 my-10">
            <div
              v-for="(framework, index) in frameworks"
              :key="index"
              class="flex flex-col items-center"
            >
              <img
                :src="framework.image"
                :alt="framework.name"
                class="w-20 h-20 mx-5 md:w-20 md:h-20"
              />
              <p class="text-sm mt-2">{{ framework.name }}</p>
            </div>
          </div>
        </div>
      </div>

      <div
        class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-full h-full"
      >
        <div
          class="flex flex-col rounded-lg w-full h-full bg-[#0D0C21] flex items-center text-white px-20 md:px-0"
        >
          <p class="text-3xl font-bold mt-2">Design Tools</p>

          <div class="grid grid-cols-2 gap-20 my-10">
            <div
              v-for="(designTool, index) in designTools"
              :key="index"
              class="flex flex-col items-center"
            >
              <img
                :src="designTool.image"
                :alt="designTool.name"
                class="w-20 h-20 mx-5 md:w-20 md:h-20"
              />
              <p class="text-sm mt-2">{{ designTool.name }}</p>
            </div>
          </div>
        </div>
      </div>

      <div
        class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-full h-full"
      >
        <div
          class="flex flex-col rounded-lg w-full h-full bg-[#0D0C21] flex items-center text-white px-20 md:px-0"
        >
          <p class="text-3xl font-bold mt-2">Technologies</p>

          <div class="grid grid-cols-2 gap-20 my-10">
            <div
              v-for="(technology, index) in technologies"
              :key="index"
              class="flex flex-col items-center"
            >
              <img
                :src="technology.image"
                :alt="technology.name"
                class="w-20 h-20 mx-5 md:w-20 md:h-20"
              />
              <p class="text-sm mt-2">{{ technology.name }}</p>
            </div>
          </div>
        </div>
      </div>

      <div
        class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-full h-full"
      >
        <div
          class="flex flex-col rounded-lg w-full h-full bg-[#0D0C21] flex items-center text-white px-5 md:px-0"
        >
          <p class="text-3xl font-bold mt-2">Soft Skills</p>

          <div class="grid grid-cols-2 gap-10 my-10">
            <div
              v-for="(softSkill, index) in softSkills"
              :key="index"
              class="flex flex-col items-left"
            >
              <p class="flex items-center gap-2 font-semibold">
                <span
                  class="w-3 h-3 rounded-lg bg-gradient-to-r from-red-500 to-red-900"
                ></span
                >{{ softSkill }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped></style>
