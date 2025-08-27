<script setup lang="ts">
import Intro from './Intro.vue';
import AboutMe from './AboutMe.vue';
import SkillsTools from './SkillsTools.vue';
import Projects from './Projects.vue';
import Educations from './Educations.vue';
import ContactMe from './ContactMe.vue';

</script>

<template>
  <main class="w-full items-center flex flex-col md:gap-70 gap-40 md:mt-40 mt-30 px-5 md:px-20 md:text-left t">
    <Intro />
    <AboutMe id="aboutme" />
    <SkillsTools id="skills&tools" />
    <Projects id="projects" />
    <Educations id="education" />
    <ContactMe id="contactme" />
  </main>
</template>

<style scoped>

</style>