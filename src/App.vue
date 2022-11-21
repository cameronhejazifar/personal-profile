<script setup>
import NavigationHeader from '@/components/NavigationHeader.vue'
import AboutView from '@/views/AboutView.vue'
import ExperienceView from '@/views/ExperienceView.vue'
import ProjectsView from '@/views/ProjectsView.vue'
import ContactView from '@/views/Contact.vue'
import FooterView from '@/views/FooterView.vue'
import ScrollDownArrows from '@/components/ScrollDownArrows.vue'
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
  <ScrollDownArrows :class="{'scroll-arrows-container': true, 'hidden': hasUserScrolled}"/>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      hasUserScrolled: false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.onWindowScroll);
  },
  unmounted() {
    window.removeEventListener('scroll', this.onWindowScroll);
  },
  methods: {
    onWindowScroll() {
      this.hasUserScrolled = true;
    }
  }
}
</script>

<style scoped>
.scroll-arrows-container {
  opacity: 1.0;
  pointer-events: none;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
  transition: opacity 200ms ease-in-out;
}

.scroll-arrows-container.hidden {
  opacity: 0.0;
}
</style>
