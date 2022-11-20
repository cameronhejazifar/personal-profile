<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue'
</script>

<template>
  <!-- TODO: implement page -->
  <div id="projects" class="fitted-container">
    <AnimateOnScroll invisible-class="animate-on-scroll-from-right">
      <div>projects</div>
    </AnimateOnScroll>
  </div>
</template>

<script>
export default {
  name: 'ProjectsView'
}
</script>

<style scoped>
</style>
