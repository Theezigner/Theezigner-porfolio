<script setup lang="ts">
type Socials = {
  icon: string;
  name: string;
  link: string;
};
const socials: Socials[] = [
  {
    icon: "/Mail.svg",
    name: "Email",
    link: "mailto:adebayotemitayo86@gmail.com",
  },
  {
    icon: "/c927d61a-fcd4-4b3b-85c8-fb7bf436c4aa-removebg-preview.png",
    name: "GitHub",
    link: "https://github.com/Theezigner",
  },
  {
    icon: "/Linkedin_White_Icon__Linkedin_Icons__White_Icons__Black_And_White_PNG_and_Vector_with_Transparent_Background_for_Free_Download-removebg-preview.png",
    name: "LinkedIn",
    link: "https://www.linkedin.com/in/temitayo-adebayo-95244b239/",
  },
  {
    icon: "/f91779ec-95b6-4188-a523-8a0a989ae40e-removebg-preview.png",
    name: "X",
    link: "https://x.com/TeeTriple64473",
  },
];
</script>

<template>
  <main class="flex flex-col gap-8 justify-center items-center w-full">
    <h2 class="font-bold text-4xl md:text-5xl">
      Contact
      <span
        class="bg-gradient-to-r from-red-500 to-red-900 bg-clip-text text-transparent"
        >ME</span
      >
    </h2>

    <div class="flex items-center gap-6 flex-wrap mb-10">
      <a
        v-for="(social, index) in socials"
        :key="index"
        :href="social.link"
        target="_blank"
        rel="noopener noreferrer"
        class="inline-flex"
        :aria-label="social.name"
      >
        <img
          :src="social.icon"
          :alt="social.name"
          class="w-10 h-10 hover:scale-110 transition-transform duration-300"
        />
      </a>
    </div>
  </main>
</template>

<style scoped></style>
