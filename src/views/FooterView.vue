<script setup>
import FooterEmail from '@/components/FooterEmail.vue'
import FooterSocialIcons from '@/components/FooterSocialIcons.vue'
</script>

<template>
  <footer>
    <div class="footer-links">
      <FooterSocialIcons/>
      <FooterEmail/>
    </div>
    <div class="attribution">
      Designed &amp; Created by Cameron Hejazi-Far
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterView',
}
</script>

<style scoped>
footer {
  display: block;
  margin-top: 10vh;
  padding-top: 10vh;
  padding-bottom: 48px;
  background: var(--color-secondary-15);
}

.footer-links {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  flex-wrap: nowrap;
}

.attribution {
  display: block;
  margin: 0 auto;
  padding: 40px 0;
  text-align: center;
  font-size: 16px;
  color: var(--color-secondary);
}

@media (max-width: 768px) {
  .footer-links {
    flex-direction: column;
    justify-content: center;
  }
}
</style>