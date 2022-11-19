<template>
  <a :href="'#' + anchor" class="nav-link" @click="$emit('selected')">
    <span class="nav-link-index">{{ paddedIndex }}</span>
    {{ title }}
  </a>
</template>

<script>
export default {
  name: 'NavigationLink',
  emits: ['selected'],
  props: {
    anchor: {type: String, required: true},
    index: {type: Number, required: true},
    title: {type: String, required: true}
  },
  computed: {
    paddedIndex() {
      return String(this.index).padStart(2, '0') + '.';
    }
  }
}
</script>

<style scoped>
.nav-link {
  color: var(--color-text);
  text-decoration: none;
  margin-left: 32px;
  font-size: 16px;
  outline: none;
  transition: color 250ms ease-in-out;
}

.nav-link-index {
  color: var(--color-secondary);
  transition: color 250ms ease-in-out;
  font-family: var(--font-mono);
  font-size: 14px;
}

.nav-link:hover {
  color: var(--color-secondary);
}

.nav-link:active, .nav-link:active .nav-link-index,
.nav-link:focus, .nav-link:focus .nav-link-index {
  color: var(--color-secondary-alt);
}

@media (max-width: 768px) {
  .nav-link {
    display: block;
    margin: 20px 0;
    font-size: 26px;
    text-align: left;
  }
  .nav-link-index {
    font-size: 20px;
  }
}
</style>