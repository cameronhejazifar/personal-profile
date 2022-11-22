<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue'
import Project from '@/components/Project.vue'
import AnchorHeader from '@/components/AnchorHeader.vue'
</script>

<template>
  <div class="fitted-container">
    <div id="projects" class="anchor"></div>
    <AnimateOnScroll animation-class="animate-on-scroll-from-left">
      <div class="anchor-container">
        <AnchorHeader :index="3" anchor="projects" title="Personal Projects"/>
      </div>
    </AnimateOnScroll>
    <Project :even="false" image="/src/assets/screenshot-macros.png" project-name="Efficient Nutrition" platform="Web"
             :links="macrosLinks">
      <p>
        Keep track of your personal progress on becoming healthier. Learn more about your eating habits by logging
        your meals, keeping track of recipes, and planning your eating.
      </p>
      <p class="footnote">
        &bull; Built using Laravel and Vue with TailwindCSS
      </p>
    </Project>
    <Project :even="true" image="/src/assets/screenshot-xfitpr.png" project-name="XFit PR"
             platform="iOS, Android, &amp; Web" :links="xFitPrLinks">
      <p>
        An application built to log your gym workouts, track and chart your progress, and learn all of the movements
        and techniques used in everyday workouts.
      </p>
      <p class="footnote">
        &bull; Mobile application built using native iOS and Android
      </p>
      <p class="footnote">
        &bull; Application API and website built using PHP
      </p>
    </Project>
    <Project :even="false" image="/src/assets/screenshot-sizetrader.png" project-name="Size Trader"
             platform="iOS, Android, &amp; Web" :links="sizeTraderLinks">
      <p>
        A social networking application where you can create and share wish lists with your friends and family, manage
        your sizes for clothing, shoes, etc., and keep track of your birthday and holiday shopping needs.
      </p>
      <p class="footnote">
        &bull; Mobile application built using native iOS and Android
      </p>
      <p class="footnote">
        &bull; Back-end and website initially built with PHP. Re-written using the .NET framework with C#
      </p>
    </Project>
    <Project :even="true" image="/src/assets/screenshot-pokedex.png" project-name="PokéDexter"
             platform="iOS &amp; Android" :links="pokeDexterLinks">
      <p>
        A companion app to help you complete your Pokédex and build the strongest team for all generations of
        main-line Pokémon games. Includes all information for every Pokémon including movesets, IVs, encounter
        locations, TMs/HMs, a typechart, and much more.
      </p>
      <p class="footnote">
        &bull; Mobile application built using native iOS and Android
      </p>
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

.footnote {
  color: var(--color-text-50);
  font-size: 12px;
  font-style: italic;
}
</style>
