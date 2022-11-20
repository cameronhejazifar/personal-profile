<script setup>
import SocialIconFacebook from '@/components/images/SocialIconFacebook.vue'
import SocialIconGithub from '@/components/images/SocialIconGithub.vue'
import SocialIconLinkedIn from '@/components/images/SocialIconLinkedIn.vue'
import SocialIconInstagram from '@/components/images/SocialIconInstagram.vue'
import SocialIconLinkTree from '@/components/images/SocialIconLinkTree.vue'
</script>

<template>
  <div class="footer-social-icons">
    <!-- Line -->
    <span class="line"></span>

    <!-- Github Icon -->
    <a href="https://github.com/cameronhejazifar" target="_blank" class="social-icon">
      <SocialIconGithub/>
    </a>

    <!-- LinkedIn Icon -->
    <a href="https://www.linkedin.com/in/cameron-hejazi" target="_blank" class="social-icon">
      <SocialIconLinkedIn/>
    </a>

    <!-- Instagram Icon -->
    <a href="https://www.instagram.com/cameronhejazi" target="_blank" class="social-icon">
      <SocialIconInstagram/>
    </a>

    <!-- Facebook Icon -->
    <a href="https://www.facebook.com/cameron7113" target="_blank" class="social-icon">
      <SocialIconFacebook/>
    </a>

    <!-- Linktree Icon -->
    <a href="https://linktr.ee/cameronhejazifar" target="_blank" class="social-icon">
      <SocialIconLinkTree/>
    </a>
  </div>
</template>

<script>
export default {
  name: 'FooterSocialIcons',
}
</script>

<style scoped>
.footer-social-icons {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
  flex-wrap: nowrap;
}

.line {
  display: block;
  width: 10vw;
  height: 1px;
  background: var(--color-text-50);
}

.social-icon {
  display: block;
  margin-left: 25px;
  width: 28px;
  height: 28px;
  color: var(--color-text-50);
  text-decoration: none;
  outline: none;
  border: none;
  transition: color 250ms ease-in-out, transform 250ms ease-in-out;
  border-radius: 2px;
}

.social-icon:hover {
  color: var(--color-primary);
  transform: scale(1.25);
}

.social-icon:focus:not(:active):not(:hover) {
  outline: 1px dashed var(--color-primary);
}

.social-icon svg {
  width: 100%;
  height: 100%;
}

@media (max-width: 768px) {
  .line {
    display: none;
  }

  .social-icon:nth-child(2) {
    margin-left: 0;
  }
}
</style>