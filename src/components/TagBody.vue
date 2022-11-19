<template>
  <div class="tag-wrapper">
    <span class="tag-prefix">&lt;body&gt;</span>
    <div class="indented-content">
      <slot/>
    </div>
    <span class="tag-suffix">&lt;body/&gt;</span>
  </div>
</template>

<style scoped>
.tag-prefix {
  display: block;
  font-family: var(--font-mono);
  color: var(--color-text-25);
  font-size: 1rem;
  margin-top: 10px;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.tag-suffix {
  display: block;
  font-family: var(--font-mono);
  color: var(--color-text-25);
  font-size: 1rem;
  padding-top: 20px;
  margin-bottom: -10px;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.indented-content {
  margin-left: 3rem;
}

.tag-wrapper {
  padding-top: 20px;
  padding-bottom: 20px;
  position: relative;
}

.tag-wrapper::before {
  content: '<html>';
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

.tag-wrapper::after {
  content: '<html/>';
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