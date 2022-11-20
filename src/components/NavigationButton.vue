<template>
  <a :href="href" class="nav-button" target="_blank">
    {{ title }}
  </a>
</template>

<script>
export default {
  name: 'NavigationButton',
  props: {
    href: {type: String, required: true},
    title: {type: String, required: true}
  },
}
</script>

<style scoped>
.nav-button {
  margin-left: 32px;
  padding: 8px 16px;
  font-size: 16px;
  color: var(--color-primary);
  border: 1px solid var(--color-primary);
  border-radius: 5px;
  text-align: center;
  text-decoration: none;
  outline: none;
  transition: color 250ms ease-in-out, background-color 250ms ease-in-out, border 250ms ease-in-out, padding 250ms ease-in-out;
}

.nav-button:hover {
  background-color: var(--color-primary-15);
  border: 3px solid var(--color-primary);
  padding: 6px 14px;
}

.nav-button:active {
  background-color: var(--color-primary-25);
}

.nav-button:focus:not(:hover):not(:active) {
  border: 1px dashed var(--color-primary);
}

@media (max-width: 768px) {
  .nav-button {
    display: block;
    margin: 30px 0;
    font-size: 26px;
  }
}
</style>