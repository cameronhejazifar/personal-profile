<script setup>
import NavigationLink from '@/components/NavigationLink.vue'
import NavigationButton from '@/components/NavigationButton.vue'
import HamburgerIcon from '@/components/HamburgerIcon.vue';
</script>

<template>
  <header :class="{'expanded': isNavExpanded}">
    <!-- Logo -->
    <a href="/" class="logo">
      <img alt="Logo" src="@/assets/logo.svg" width="48" height="48"/>
    </a>

    <!-- Hamburger Menu (Mobile) -->
    <button class="nav-hamburger" @click.prevent.stop="onHamburgerClick">
      <HamburgerIcon :expanded="isNavExpanded"/>
    </button>

    <!-- Nav Links -->
    <nav>
      <NavigationLink :index="1" anchor="about" title="About" @selected="setNavExpanded(false)"/>
      <NavigationLink :index="2" anchor="experience" title="Experience" @selected="setNavExpanded(false)"/>
      <NavigationLink :index="3" anchor="projects" title="Projects" @selected="setNavExpanded(false)"/>
      <NavigationLink :index="4" anchor="contact" title="Contact" @selected="setNavExpanded(false)"/>

      <!-- Resume -->
      <NavigationButton href="/go-to-resume" title="Resume"/>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'NavigationHeader',
  data() {
    return {
      isNavExpanded: false
    }
  },
  methods: {
    onHamburgerClick() {
      this.setNavExpanded(!this.isNavExpanded);
      let el = document.querySelector(':focus');
      if (el) {
        el.blur();
      }
    },
    setNavExpanded(expanded) {
      this.isNavExpanded = expanded;
      // Determine if the root element of the page should disable scrolling
      if (this.isNavExpanded) {
        document.body.classList.add('nav-expanded');
      } else {
        document.body.classList.remove('nav-expanded');
      }
    }
  }
}
</script>

<style scoped>
header {
  position: fixed;
  width: 100%;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 0;
  height: var(--dimension-header-height);
  background-color: var(--color-background-90);
  overflow: hidden;
  z-index: 1000;
}

@supports ((-webkit-backdrop-filter: none) or (backdrop-filter: none)) {
  header {
    background-color: var(--color-background-25);
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);
  }
}

.logo {
  display: flex;
  align-items: center;
  justify-content: center;
  height: var(--dimension-header-height);
  width: var(--dimension-header-height);
  outline: none;
  border: none;
  text-decoration: none;
}

.logo:focus:not(:hover):not(:active) {
  border: 1px dotted var(--color-secondary);
}

nav {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
  flex-wrap: nowrap;
  margin-right: 16px;
}

.nav-hamburger {
  display: none;
  justify-content: center;
  align-items: center;
  width: var(--dimension-header-height);
  height: var(--dimension-header-height);
  background: transparent;
  border: none;
  text-decoration: none;
  outline: none;
  cursor: pointer;
}

.nav-hamburger:focus:not(:hover):not(:active) {
  border: 1px dotted var(--color-secondary);
}

@media (max-width: 768px) {
  .nav-hamburger {
    display: flex;
  }

  header {
    align-items: flex-start;
    transition: height 500ms ease;
  }

  header.expanded {
    height: 100vh;
    overflow: hidden;
  }

  nav {
    margin-left: 16px;
    flex-basis: 100%;
    align-items: stretch;
    justify-content: flex-start;
    flex-direction: column;
    flex-wrap: nowrap;
    height: calc(100vh - var(--dimension-header-height));
    overflow: scroll;
  }
}
</style>
