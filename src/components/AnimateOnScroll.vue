<!--suppress CssUnusedSymbol -->
<template>
  <div ref="animateDiv"
       :class="{[animationClass ?? 'animate-on-scroll-from-bottom']: true, [visibleClass ?? 'animate-on-scroll-visible']: isVisible}">
    <slot/>
  </div>
</template>

<script>
export default {
  name: 'AnimateOnScroll',
  props: {
    animationClass: {
      type: String,
      required: false
    },
    visibleClass: {
      type: String,
      required: false
    }
  },
  data() {
    return {
      observer: null,
      isVisible: false
    }
  },
  mounted() {
    this.observer = new IntersectionObserver(entries => {
      entries.forEach(entry => this.isVisible = entry.isIntersecting);
    }, {
      root: null,
      rootMargin: '0px',
      threshold: 0
    });
    this.observer.observe(this.$refs.animateDiv);
  },
  unmounted() {
    if (this.$refs.animateDiv) {
      this.observer.unobserve(this.$refs.animateDiv);
    }
  }
}
</script>

<style scoped>
.animate-on-scroll-from-bottom {
  opacity: 0;
  visibility: hidden;
  transform: translateY(20vh);
  transition: opacity 1200ms ease-out, transform 600ms ease-out,
  visibility 1200ms ease-out;
  will-change: opacity, transform, visibility;
}

.animate-on-scroll-from-left {
  opacity: 0;
  visibility: hidden;
  transform: translateX(-30vw);
  transition: opacity 1200ms ease-out, transform 600ms ease-out,
  visibility 1200ms ease-out;
  will-change: opacity, transform, visibility;
}

.animate-on-scroll-from-right {
  opacity: 0;
  visibility: hidden;
  transform: translateX(30vw);
  transition: opacity 1200ms ease-out, transform 600ms ease-out,
  visibility 1200ms ease-out;
  will-change: opacity, transform, visibility;
}

.animate-on-scroll-visible {
  opacity: 1;
  transform: none;
  visibility: visible;
}
</style>