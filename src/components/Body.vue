<script setup lang="ts">
import Intro from './Intro.vue';
import AboutMe from './AboutMe.vue';
import SkillsTools from './SkillsTools.vue';
import Projects from './Projects.vue';
import Educations from './Educations.vue';
import ContactMe from './ContactMe.vue';

</script>

<template>
  <main class="w-full items-center flex flex-col md:gap-50 gap-40 md:mt-40 mt-30 px-5 md:px-20 md:text-left t">
    <Intro />
    <AboutMe id="aboutme" class="scroll-pt-24" />
    <SkillsTools id="skills&tools" class="scroll-pt-24" />
    <Projects id="projects" class="scroll-pt-24" />
    <Educations id="education" class="scroll-pt-24" />
    <ContactMe id="contactme" class="scroll-pt-24" />
  </main>
</template>

<style scoped>
  html {
  scroll-behavior: smooth;
}
</style>