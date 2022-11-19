<template>
  <div class="typed-out-container">
    <div class="typed-out">
      <slot/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TypewriterText'
}
</script>

<style scoped>
.typed-out-container {
  display: inline-block;
}

.typed-out {
  overflow: hidden;
  padding-right: 15px;
  border-right: .15em solid var(--color-secondary);
  white-space: nowrap;
  animation: typing 2000ms steps(20, end) forwards, blinking 1500ms infinite;
  width: 0;
}

@keyframes typing {
  from {
    width: 0
  }
  to {
    width: 100%
  }
}

@keyframes blinking {
  from {
    border-color: transparent;
  }
  to {
    border-color: var(--color-secondary);
  }
}
</style>