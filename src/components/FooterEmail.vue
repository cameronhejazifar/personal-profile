<template>
  <div class="footer-email">
    <!-- Email Compose Link -->
    <a href="mailto:cameron@hejazi-far.com">cameron@hejazi-far.com</a>

    <!-- Line -->
    <span class="line"></span>
  </div>
</template>

<script>
export default {
  name: 'FooterEmail'
}
</script>

<style scoped>
.footer-email {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  flex-wrap: nowrap;
}

.line {
  display: block;
  width: 10vw;
  height: 2px;
  margin-left: 10px;
  background: var(--color-text-25);
}

.footer-email a {
  display: block;
  color: var(--color-text-50);
  text-decoration: none;
  outline: none;
  border: none;
  font-size: 16px;
  margin-bottom: 3px;
  transition: color 250ms ease-in-out, transform 250ms ease-in-out;
}

.footer-email a:hover {
  color: var(--color-primary);
  transform: scale(1.05);
}

.footer-email a:focus:not(:active):not(:hover) {
  outline: 1px dashed var(--color-primary);
}

@media (max-width: 768px) {
  .line {
    display: none;
  }

  .footer-email a {
    margin-top: 16px;
  }
}
</style>