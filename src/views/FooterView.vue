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
      <a href="https://github.com/cameronhejazifar/personal-profile" target="_blank">
        Designed &amp; Created by Cameron Hejazi-Far
      </a>
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
}

.attribution a {
  display: block;
  margin: 0 auto;
  font-size: 16px;
  color: var(--color-secondary);
  text-decoration: none;
  outline: none;
  border: none;
  border-radius: 2px;
  text-align: center;
  transition: color 250ms ease-in-out, transform 250ms ease-in-out;
}

.attribution a:hover {
  color: var(--color-primary);
  transform: scale(1.05);
}

.attribution a:focus:not(:active):not(:hover) {
  outline: 1px dashed var(--color-primary);
}

@media (max-width: 768px) {
  .footer-links {
    flex-direction: column;
    justify-content: center;
  }
}
</style>