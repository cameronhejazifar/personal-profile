<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue'
import ProgrammingLanguagesGrid from '@/components/ProgrammingLanguagesGrid.vue'
import AnchorHeader from '@/components/AnchorHeader.vue'
</script>


<template>
  <!-- TODO: implement page -->
  <div class="fitted-container">
    <div id="experience" class="anchor"></div>
    <AnimateOnScroll>
      <div class="anchor-container">
        <AnchorHeader :index="2" title="Experience"/>
      </div>
      <ProgrammingLanguagesGrid/>
    </AnimateOnScroll>
  </div>
</template>

<script>
export default {
  name: 'ExperienceView'
}
</script>

<style scoped>
.fitted-container {
  padding-top: 128px;
}
.anchor-container {
  display: block;
  width: 810px;
  max-width: 90%;
  margin: 0 auto;
}
</style>
