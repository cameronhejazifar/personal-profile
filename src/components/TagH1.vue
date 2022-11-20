<template>
  <h1><slot/></h1>
</template>

<style scoped>
h1 {
  color: var(--color-text);
  font-weight: 400;
  position: relative;
  margin-top: 40px;
  margin-bottom: 40px;
  padding-left: 1rem;
  font-size: 2.5rem;
  line-height: 4rem;
}

h1::before {
  content: '<h1>';
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

h1::after {
  content: '<h1/>';
  font-family: var(--font-mono);
  color: var(--color-text-25);
  font-size: 1rem;
  position: absolute;
  left: -1rem;
  bottom: -2.25rem;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
</style>