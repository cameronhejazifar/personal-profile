<template>
  <h3 class="anchor-header">
    <span class="anchor-header-index">{{ paddedIndex }}</span>
    {{ title }}
  </h3>
</template>

<script>
export default {
  name: 'AnchorHeader',
  props: {
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
.anchor-header {
  display: block;
  padding: 0;
  margin: 0;
  color: var(--color-text);
  text-decoration: none;
  font-size: 24px;
  outline: none;
  transition: color 250ms ease-in-out;
  cursor: default;
}

.anchor-header-index {
  color: var(--color-secondary);
  transition: color 250ms ease-in-out;
  font-size: 20px;
}

.anchor-header:hover {
  color: var(--color-secondary);
}

.anchor-header:active, .anchor-header:active .anchor-header-index,
.anchor-header:focus, .anchor-header:focus .anchor-header-index {
  color: var(--color-secondary-alt);
}
</style>