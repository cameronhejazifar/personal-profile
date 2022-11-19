<template>
  <h2><slot/></h2>
</template>

<style scoped>
h2 {
  color: var(--color-text);
  font-weight: 400;
  position: relative;
  margin-top: 40px;
  margin-bottom: 40px;
  font-size: 3rem;
  line-height: 4rem;
}

h2::before {
  content: '<h2>';
  font-family: var(--font-mono);
  color: var(--color-text-25);
  font-size: 1rem;
  position: absolute;
  margin-top: -2.5rem;
  left: -1rem;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

h2::after {
  content: '<h2/>';
  font-family: var(--font-mono);
  color: var(--color-text-25);
  font-size: 1rem;
  position: absolute;
  left: -1rem;
  bottom: -2.75rem;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
</style>