<template>
  <p><slot/></p>
</template>

<style scoped>
p {
  color: var(--color-text-50);
  font-weight: 400;
  position: relative;
  margin-top: 0;
  padding-top: 30px;
  margin-bottom: 20px;
  font-size: 1rem;
  line-height: 1.5rem;
}

p::before {
  content: '<p>';
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

p::after {
  content: '<p/>';
  font-family: var(--font-mono);
  color: var(--color-text-25);
  font-size: 1rem;
  position: absolute;
  left: -1rem;
  bottom: -1.75rem;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
</style>