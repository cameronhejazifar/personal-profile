<script setup>
import NavigationHeader from '@/components/NavigationHeader.vue'
import AboutView from '@/views/AboutView.vue'
import ExperienceView from '@/views/ExperienceView.vue';
import ProjectsView from '@/views/ProjectsView.vue';
import ContactView from '@/views/Contact.vue';
import FooterView from '@/views/FooterView.vue';
</script>

<template>
  <NavigationHeader/>
  <main>
    <AboutView/>
    <ExperienceView/>
    <ProjectsView/>
    <ContactView/>
    <FooterView/>
  </main>
</template>

<style scoped>
</style>
