<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue'
import ProgrammingLanguagesGrid from '@/components/ProgrammingLanguagesGrid.vue'
import AnchorHeader from '@/components/AnchorHeader.vue'
import EmploymentHistoryCards from '@/components/EmploymentHistoryCards.vue'
</script>


<template>
  <div class="fitted-container">
    <div id="experience" class="anchor"></div>
    <AnimateOnScroll animation-class="animate-on-scroll-from-left">
      <div class="anchor-container">
        <AnchorHeader :index="2" anchor="experience" title="Experience"/>
      </div>
    </AnimateOnScroll>
    <EmploymentHistoryCards/>
    <AnimateOnScroll>
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
  max-width: 90%;
  margin: 0 auto;
}
</style>
