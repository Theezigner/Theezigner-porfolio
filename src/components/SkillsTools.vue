<script setup lang="ts">
type Skill = {
  image: string;
  name: string;
};

type SkillCategory = {
  heading: string;
  skills: Skill[];
};

type SoftSkillCategory = {
  heading: string;
  skills: string[];
};

const skillCategories: SkillCategory[] = [
  {
    heading: "Languages",
    skills: [
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
    ],
  },
  {
    heading: "Frameworks/Build Tools",
    skills: [
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
        image: "/skills/vite.svg",
        name: "Vite",
      },
      {
        image: "/skills/Tailwind Css.svg",
        name: "Tailwind CSS",
      },
    ],
  },
  {
    heading: "Design Tools",
    skills: [
      {
        image:
          "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg",
        name: "Figma",
      },
      {
        image:
          "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/photoshop/photoshop-original.svg",
        name: "Photoshop",
      },
      {
        image:
          "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/illustrator/illustrator-original.svg",
        name: "Illustrator",
      },
      {
        image:
          "https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/canva/canva-original.svg",
        name: "Canva",
      },
    ],
  },
  {
    heading: "Technologies",
    skills: [
      {
        image:
          "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg",
        name: "Git",
      },
      {
        image: "/contacts/Github.svg",
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
    ],
  },
];

const softSkillsData: SoftSkillCategory = {
  heading: "Soft Skills",
  skills: [
    "Team Collaboration",
    "Debugging",
    "Problem-Solving",
    "Effective Communication",
    "Adaptability",
    "Time Management",
  ],
};
</script>

<template>
  <main
    id="skills&tools"
    class="w-full flex flex-col items-center justify-center text-center md:items-start md:text-left"
  >
    <h2 class="font-bold text-4xl md:text-5xl pt-30">Skills & Tools</h2>

    <section
      class="grid grid-cols-1 md:grid-cols-2 justify-between gap-10 md:gap-10 mt-10 md:w-full md:h-full"
    >
      <div
        v-for="(category, index) in skillCategories"
        :key="index"
        class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-full h-full"
      >
        <div
          class="flex flex-col rounded-lg w-full h-full bg-[#0D0C21] flex items-center text-white"
        >
          <p class="text-2xl lg:text-3xl font-bold mt-2">{{ category.heading }}</p>

          <div class="grid grid-cols-2 md:gap-20 gap-10 my-10">
            <div
              v-for="(skill, skillIndex) in category.skills"
              :key="skillIndex"
              class="flex flex-col items-center"
            >
              <img
                :src="skill.image"
                :alt="skill.name"
                class="w-15 h-15 md:w-20 md:h-20 mx-5 md:w-20 md:h-20"
              />
              <p class="text-sm mt-2">{{ skill.name }}</p>
            </div>
          </div>
        </div>
      </div>

      <div
        class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-full h-full"
      >
        <div
          class="flex flex-col rounded-lg w-full h-full bg-[#0D0C21] flex items-center text-white px-5"
        >
          <p class="text-2xl lg:text-3xl font-bold mt-2">{{ softSkillsData.heading }}</p>

          <div class="grid lg:grid-cols-2 gap-5 my-10">
            <div
              v-for="(softSkill, index) in softSkillsData.skills"
              :key="index"
              class="flex flex-col items-left"
            >
              <div
                class="flex flex-row flex-wrap items-center gap-2 gap-1 md:gap-2 font-semibold text-left text-xs md:text-sm"
              >
                <div
                  class="md:w-3 md:h-3 w-2 h-2 rounded-lg bg-gradient-to-r from-red-500 to-red-900"
                ></div>
                <p class="">
                  {{ softSkill }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped></style>
