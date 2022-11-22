<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue'
import Project from '@/components/Project.vue'
import AnchorHeader from '@/components/AnchorHeader.vue'
</script>

<template>
  <div class="fitted-container">
    <div id="projects" class="anchor"></div>
    <AnimateOnScroll animation-class="animate-on-scroll-from-bottom">
      <div class="anchor-container">
        <AnchorHeader :index="3" anchor="projects" title="Personal Projects"/>
      </div>
    </AnimateOnScroll>
    <!-- TODO: replace placeholder content here -->
    <Project :even="false" image="/src/assets/screenshot-sizetrader.png" project-name="Size Trader"
             platform="iOS, Android, & Web" :links="sizeTraderLinks">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc rhoncus nunc ac neque tempor, quis lobortis dui
      tincidunt. Nam porta porta nisi. Phasellus sagittis dui quis tellus aliquam vestibulum at eget justo. Fusce
      scelerisque, mauris sit amet ornare interdum, nibh est maximus lorem, non laoreet felis lectus sed lacus. Ut
      non sollicitudin enim, non finibus justo. Nam massa tortor, aliquet in sodales ultrices, varius eu turpis.
      Vivamus vel malesuada sem. Cras et tincidunt ex, sed ultricies nisi.
    </Project>
    <!-- TODO: replace placeholder content here -->
    <Project :even="true" image="/src/assets/screenshot-xfitpr.png" project-name="XFit PR"
             platform="iOS, Android, & Web" :links="xFitPrLinks">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc rhoncus nunc ac neque tempor, quis lobortis dui
      tincidunt. Nam porta porta nisi. Phasellus sagittis dui quis tellus aliquam vestibulum at eget justo. Fusce
      scelerisque, mauris sit amet ornare interdum, nibh est maximus lorem, non laoreet felis lectus sed lacus. Ut
      non sollicitudin enim, non finibus justo. Nam massa tortor, aliquet in sodales ultrices, varius eu turpis.
      Vivamus vel malesuada sem. Cras et tincidunt ex, sed ultricies nisi.
    </Project>
    <!-- TODO: replace placeholder content here -->
    <Project :even="false" image="/src/assets/screenshot-macros.png" project-name="Efficient Nutrition" platform="Web" :links="macrosLinks">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc rhoncus nunc ac neque tempor, quis lobortis dui
      tincidunt. Nam porta porta nisi. Phasellus sagittis dui quis tellus aliquam vestibulum at eget justo. Fusce
      scelerisque, mauris sit amet ornare interdum, nibh est maximus lorem, non laoreet felis lectus sed lacus. Ut
      non sollicitudin enim, non finibus justo. Nam massa tortor, aliquet in sodales ultrices, varius eu turpis.
      Vivamus vel malesuada sem. Cras et tincidunt ex, sed ultricies nisi.
    </Project>
    <!-- TODO: replace placeholder content here -->
    <Project :even="true" image="/src/assets/screenshot-pokedex.png" project-name="PokéDexter" platform="Android" :links="pokeDexterLinks">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc rhoncus nunc ac neque tempor, quis lobortis dui
      tincidunt. Nam porta porta nisi. Phasellus sagittis dui quis tellus aliquam vestibulum at eget justo. Fusce
      scelerisque, mauris sit amet ornare interdum, nibh est maximus lorem, non laoreet felis lectus sed lacus. Ut
      non sollicitudin enim, non finibus justo. Nam massa tortor, aliquet in sodales ultrices, varius eu turpis.
      Vivamus vel malesuada sem. Cras et tincidunt ex, sed ultricies nisi.
    </Project>
  </div>
</template>

<script>
export default {
  name: 'ProjectsView',
  computed: {
    sizeTraderLinks() {
      return [
        {label: 'Website', url: 'https://sizetrader.com'}
      ];
    },
    xFitPrLinks() {
      return [
        {label: 'Website', url: 'https://xfit-pr.com'}
      ];
    },
    macrosLinks() {
      return [
        {label: 'Website', url: 'https://macros.hejazi-far.com'}
      ];
    },
    pokeDexterLinks() {
      return [];
    }
  }
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
