<script setup>
import NavigationHeader from '@/components/NavigationHeader.vue'
import AboutView from '@/views/AboutView.vue'
import ExperienceView from '@/views/ExperienceView.vue';
import ProjectsView from '@/views/ProjectsView.vue';
import ContactView from '@/views/Contact.vue';
</script>

<template>
  <NavigationHeader/>
  <main>
    <AboutView/>
    <ExperienceView/>
    <ProjectsView/>
    <ContactView/>
  </main>
</template>

<style scoped>
</style>
