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
    image: "/projects/pokemon card.png",
    title: "Pokemon Card Display",
    description: "A modern, single-page application built with React.js, TypeScript, and Vite, designed to fetch, display, and manage data from the PokéAPI.The interface, which I also designed and prototyped, features a card-based UI with responsive layouts styled using Tailwind CSS. It showcases proficiency in advanced frontend practices, including efficient API data fetching with axios, robust error handling, custom skeleton loading states, and a scalable architecture utilizing TanStack Router for type-safe routing and infinite scrolling for improved user experience.",
    buildTools: ["Figma", "React","Typescipt","Vite", "TailwindCSS"],
    demoLink: "https://pokemon-card-display.vercel.app/",
    gitLink: "https://github.com/Theezigner/Pokemon-Card-Display.git",
  },
  {
    image: "/projects/Theezigner portfolio ss.png",
    title: "Theezigner's Portfolio",
    description: "A fully responsive, multi-section personal portfolio built with Vue 3 (Composition API), TypeScript, and Vite, designed to demonstrate modern Frontend Engineering proficiency.The interface was meticulously designed in Figma and implemented using Tailwind CSS for an efficient, utility-first styling approach, featuring smooth animations and a polished UI. The project highlights core development practices like component reusability and state management while leveraging Vite for a high-performance and optimized user experience.",
    buildTools: ["Figma", "Vue.js","Typescipt", "TailwindCSS"],
    demoLink: "https://theezigner-porfolio.vercel.app/",
    gitLink: "https://github.com/Theezigner/Theezigner-porfolio.git",
  },
   {
    image: "/projects/vapor Tracker.png",
    title: "Vapor Tracker ",
    description: "A high-fidelity System Dashboard (Synth-Tracker) built with React.js, TypeScript, and Vite, designed as a focused exercise in retro-futuristic, synthwave UI aesthetics.The project is a dummy application built solely for design and front-end practice; all data and interactive elements are mocked or static. It demonstrates mastery of front-end architecture and advanced aesthetic implementation, leveraging Tailwind CSS to achieve a specific, high-contrast visual language with cyan, purple, and fuchsia glowing accents, showcasing proficiency in the React ecosystem and utility-first design principles.",
    buildTools: ["Figma", "React","Typescipt", "TailwindCSS"],
    demoLink: "https://vapor-tracker.vercel.app/",
    gitLink: "https://github.com/Theezigner/vaporTracker.git",
  },
    {
    image: "/projects/space.svg",
    title: "Space Tourism Website",
    description: "A responsive, multi-section website built with Next.js 14, TypeScript, and Tailwind CSS v4, designed to demonstrate modern frontend practices. It features adaptive layouts with per-page background images, screen-size–specific image rendering, and dynamic flex ordering for mobile vs. desktop. The project highlights responsive design techniques, component reusability, and accessibility, while leveraging Next.js’ routing and optimization for a smooth developer and user experience.",
    buildTools: ["Next.js","Typescipt", "React", "TailwindCSS"],
    demoLink: "https://space-app-seven-rouge.vercel.app/",
    gitLink: "https://github.com/Theezigner/space-app.git",
  },
  {
    image: "/projects/ecommerce-product-page.jpg",
    title: "E-commerce Product Page",
    description: "A responsive, single-page product showcase inspired by Frontend Mentor challenges. It features a thumbnail-driven image gallery, a cart system with localStorage persistence, and an animated mobile hamburger menu. Built with React 19, TypeScript, Vite 7, Tailwind CSS v4, and React Router DOM v7, the project demonstrates clean state management, reusable contexts, and smooth UI transitions.",
    buildTools: ["Typescipt", "React", "TailwindCSS", "Vite"],
    demoLink: "https://ecommerce-product-page-five-sigma.vercel.app/",
    gitLink: "https://github.com/Theezigner/ecommerce-product-page.git",
  },
  {
    image: "/projects/interactive-card-details.jpg",
    title: "Interactive Card Design",
    description: "A visually interactive credit card form built with TypeScript and Tailwind CSS. Users can enter card details and instantly see the card preview update in real-time. It was developed as the first official assignment for the third semester of my frontend engineering course, with a focus on DOM manipulation, form validation, and responsive layout using modern tools.",
    buildTools: ["TypeScript", "TailwindCSS", "Vite"],
    demoLink: "https://interactive-card-design-plum.vercel.app/",
    gitLink: "https://github.com/Theezigner/interactive-card-design.git",
  },
  {
    image: "/projects/Spots App 1440px Name Overflow.svg",
    title: "SPOTS App",
    description: "A single-page social media web app built with React and Vite, designed for sharing and engaging with user-generated content. It features photo uploads with captions, editable user profiles with avatars and bios, and interactive like/unlike functionality. The project emphasizes clean state management, responsive layouts, and smooth user interactions, showcasing the core building blocks of a modern social platform.",
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
    <h2 class="font-bold text-4xl md:text-5xl pt-30">Projects</h2>

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
          <p class="text-xs lg:text-sm text-left font-normal text-gray-400 my-3">
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
