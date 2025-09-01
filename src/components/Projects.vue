<script setup lang="ts">
type Projects = {
  image: string;
  title: string;
  description: string;
  buildTools: string[];
  demoLink: string;
  gitLink: string;
};

const projects: Projects[] = [
    {
    image: "/Desktop - Home.svg",
    title: "Space Tourism Website",
    description: "A responsive, single-page product showcase inspired by Frontend Mentor challenges. It features a thumbnail-driven image gallery, a cart system with localStorage persistence, and an animated mobile hamburger menu. Built with React 19, TypeScript, Vite 7, Tailwind CSS v4, and React Router DOM v7, the project demonstrates clean state management, reusable contexts, and smooth UI transitions.",
    buildTools: ["Next.js","Typescipt", "React", "TailwindCSS"],
    demoLink: "https://space-app-seven-rouge.vercel.app/",
    gitLink: "https://github.com/Theezigner/space-app.git",
  },
  {
    image: "/ecommerce-product-page.jpg",
    title: "E-commerce Product Page",
    description: "A responsive, single-page product showcase inspired by Frontend Mentor challenges. It features a thumbnail-driven image gallery, a cart system with localStorage persistence, and an animated mobile hamburger menu. Built with React 19, TypeScript, Vite 7, Tailwind CSS v4, and React Router DOM v7, the project demonstrates clean state management, reusable contexts, and smooth UI transitions.",
    buildTools: ["Typescipt", "React", "TailwindCSS", "Vite"],
    demoLink: "https://ecommerce-product-page-five-sigma.vercel.app/",
    gitLink: "https://github.com/Theezigner/ecommerce-product-page.git",
  },
  {
    image: "/interactive-card-details.jpg",
    title: "Interactive Card Design",
    description: "A visually interactive credit card form built with TypeScript and Tailwind CSS. Users can enter card details and instantly see the card preview update in real-time. It was developed as the first official assignment for the third semester of my frontend engineering course, with a focus on DOM manipulation, form validation, and responsive layout using modern tools.",
    buildTools: ["TypeScript", "TailwindCSS", "Vite"],
    demoLink: "https://interactive-card-design-plum.vercel.app/",
    gitLink: "https://github.com/Theezigner/interactive-card-design.git",
  },
  {
    image: "/Spots App 1440px Name Overflow.svg",
    title: "SPOTS App",
    description: "A media app",
    buildTools: ["React", "TailwindCSS", "Vite"],
    demoLink: "https://spots-app-ashen.vercel.app/",
    gitLink: "https://github.com/Theezigner/spots-app.git",
  },
];
</script>

<template>
  <main
    id="projects"
    class="w-full flex flex-col justify-center text-center items-start md:text-left"
  >
    <h2 class="font-bold text-4xl md:text-5xl">Projects</h2>

    <section
      class="grid grid-cols-1 md:grid-cols-3 justify-between md:gap-5 gap-10 mt-10 w-full"
    >
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-auto h-full"
      >
        <div
          class="flex flex-col flex-wrap rounded-lg w-auto h-full bg-[#0D0C21] flex items-start text-white p-5 md:p-5"
        >
          <img
            :src="project.image"
            alt="Project Image"
            class=" rounded-t-lg"
          />

          <p class="flex gap-2 font-semibold text-2xl mt-2">
            {{ project.title }}
          </p>
          <p class="text-sm text-left font-normal text-gray-400 my-3">
            {{ project.description }}
          </p>

          <div class="flex flex-row flex-wrap gap-2">
            <div v-for="(tool, idx) in project.buildTools" :key="idx">
              <div
                class="p-[0.5px] rounded-full bg-gradient-to-r from-red-500 to-red-900 w-auto"
              >
                <div class="bg-[#0D0C21] rounded-full px-3 py-0 text-gray-200 text-xs">
                  {{ tool }}
                </div>
              </div>
            </div>
          </div>

            <div class="mt-auto w-full flex flex-row gap-2 mt-5 pt-5 ">
                <button
                class="flex-1 rounded-lg bg-gradient-to-r from-red-500 to-red-900 py-2 px-4 text-white font-semibold text-xs md:text-sm w-35"
                >
                <a :href="project.demoLink" target="_blank" rel="noopener"
                    >Live Demo</a
                >
                </button>
                <button
                class="flex-1 rounded-lg border border-white bg-transparent py-2 px-4  font-semibold text-xs md:text-sm w-35"
                >
                <a :href="project.gitLink" target="_blank" rel="noopener"
                    >GitHub Repo</a
                >
                </button>
                </div>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped></style>
