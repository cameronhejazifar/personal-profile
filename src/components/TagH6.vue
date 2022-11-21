<template>
  <h6><slot/></h6>
</template>

<style scoped>
h6 {
  color: var(--color-text);
  font-weight: 400;
  position: relative;
  margin-top: 40px;
  margin-bottom: 40px;
  padding-left: 1rem;
  font-size: 1.1rem;
  line-height: 1.75rem;
}

h6::before {
  content: '<h6>';
  font-family: var(--font-mono);
  color: var(--color-text-25);
  font-size: 1rem;
  position: absolute;
  margin-top: -1.75rem;
  left: -1rem;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

h6::after {
  content: '<h6/>';
  font-family: var(--font-mono);
  color: var(--color-text-25);
  font-size: 1rem;
  position: absolute;
  left: -1rem;
  bottom: -2rem;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
</style>