<template>
  <div class="scroll-arrows">
    <span></span>
    <span></span>
    <span></span>
  </div>
</template>

<script>
export default {
  name: 'ScrollDownArrows'
}
</script>

<style scoped>
.scroll-arrows {
  position: fixed;
  bottom: 30px;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 100;
}

.scroll-arrows span {
  display: block;
  width: 20px;
  height: 20px;
  border-bottom: 2px solid var(--color-primary);
  border-right: 2px solid var(--color-primary);
  transform: rotate(45deg);
  margin: -10px;
  animation: animate 2000ms infinite;
}

.scroll-arrows span:nth-child(2) {
  animation-delay: -200ms;
}

.scroll-arrows span:nth-child(3) {
  animation-delay: -400ms;
}

@keyframes animate {
  0% {
    opacity: 0;
    transform: rotate(45deg) translate(-40px, -40px);
  }
  50% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: rotate(45deg) translate(20px, 20px);
  }
}
</style>