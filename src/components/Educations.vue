<script setup lang="ts">
type Certificate = {
  url: string;
  type: "image" | "pdf";
  preview?: string;
};

type Educations = {
  name: string;
  years: { start: string; end: string | "Present" };
  description: string;
  certificates?: Certificate[];
};

const educations: Educations[] = [
  {
    name: "Altschool Africa",
    years: { start: "2024", end: "25" },
    description:
      "Gained hands-on experience in building modern, responsive, and scalable web applications. Learned and applied HTML, CSS, JavaScript, TypeScript, React, Vite, and Vue, along with best practices in UI/UX, performance optimization, and component-based development. Strengthened problem-solving skills through real-world projects, teamwork, and continuous learning in a fast-paced environment.",
    certificates: [
      {
        url: "/certificates/altschool/AltSchool Africa Certificate - Temitayo.pdf",
        type: "pdf",
        preview: "/certificates/altschool/certificate preview.png",
      },
      {
        url: "/certificates/altschool/Volunteer Certificate-03.jpg",
        type: "image",
      },
    ],
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
    certificates: [
      {
        url: "/certificates/coursera/Coursera Certificate.pdf",
        type: "pdf",
        preview: "/certificates/coursera/coursera preview.jpeg",
      },
    ],
  },
  {
    name: "Canva 4 E",
    years: { start: "2021", end: "21" },
    description:
      "Completed training in graphic design principles including color theory, typography, layout, and visual storytelling. Learned to create engaging digital assets such as social media graphics, presentations, and branding materials using Canva's design tools. Built a strong foundation in visual communication and creative problem-solving.",
  },
];
</script>

<template>
  <main
    id="education"
    class="w-full flex flex-col items-center justify-center text-center md:items-start md:text-left"
  >
    <h2 class="font-bold text-4xl md:text-5xl pt-30">Educations</h2>

    <section
      class="flex flex-col justify-between gap-10 mt-10 md:w-full w-full"
    >
      <div v-for="(education, index) in educations" :key="index" class="">
        <div class="mb-5 flex flex-wrap items-center gap-3">
          <div class="flex flex-row items-center gap-2 md:gap-5">
            <div class="block bg-gradient-to-r from-red-500 to-red-900 w-3 h-3 md:w-5 md:h-5 rounded-full"></div>
            <p class="text-lg md:text-4xl font-semibold text-left">
            {{ education.name }}
          </p>
          </div>
          <div
            class="rounded-lg bg-gradient-to-r from-red-500 to-red-900 py-1 px-3 text-sm md:text-2xl text-white font-semibold"
          >
            {{ education.years.start }} - {{ education.years.end }}
          </div>
        </div>
        <div
          class="p-[1px] rounded-lg bg-gradient-to-r from-red-500 to-red-900 w-full h-full ml-0 md:ml-10"
        >
          <div
            class="flex flex-col rounded-lg w-full h-full bg-[#0D0C21] flex items-start text-white px-4 py-4 md:p-5"
          >
            <p
              class="md:text-justify text-left text-xs md:text-xl font-normal text-gray-300 my-3"
            >
              {{ education.description }}
            </p>
            
            <div 
              v-if="education.certificates && education.certificates.length > 0" 
              class="mt-4 mb-3 flex flex-col md:flex-row gap-4"
            >
              <a 
                v-for="(cert, certIndex) in education.certificates" 
                :key="certIndex"
                :href="cert.url" 
                target="_blank"
                rel="noopener noreferrer"
                class="flex-1 group relative"
              >
                <template v-if="cert.type === 'pdf'">
                  <div 
                    v-if="cert.preview"
                    class="relative w-full h-32 md:h-40 rounded-lg border-2 border-gray-700 group-hover:border-red-500 transition-all duration-300 shadow-lg group-hover:shadow-red-500/50 cursor-pointer overflow-hidden"
                  >
                    <img 
                      :src="cert.preview" 
                      :alt="`${education.name} Certificate Preview`"
                      class="w-full h-full object-cover"
                    />
                   
                  </div>
                  <div 
                    v-else
                    class="w-full h-32 md:h-40 rounded-lg border-2 border-gray-700 group-hover:border-red-500 transition-all duration-300 shadow-lg group-hover:shadow-red-500/50 cursor-pointer bg-gradient-to-br from-gray-800 to-gray-900 flex flex-col items-center justify-center gap-2"
                  >
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12 md:h-16 md:w-16 text-red-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21h10a2 2 0 002-2V9.414a1 1 0 00-.293-.707l-5.414-5.414A1 1 0 0012.586 3H7a2 2 0 00-2 2v14a2 2 0 002 2z" />
                    </svg>
                    <span class="text-xs md:text-sm font-semibold text-gray-300">PDF Certificate</span>
                  </div>
                </template>
                <img 
                  v-else
                  :src="cert.url" 
                  :alt="`${education.name} Certificate ${certIndex + 1}`"
                  class="w-full h-32 md:h-40 object-cover rounded-lg border-2 border-gray-700 group-hover:border-red-500 transition-all duration-300 shadow-lg group-hover:shadow-red-500/50 cursor-pointer"
                />
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>