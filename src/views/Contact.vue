<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue'
import AnchorHeader from '@/components/AnchorHeader.vue'
import SocialIconLinkedIn from '@/components/images/SocialIconLinkedIn.vue'
import SocialIconInstagram from '@/components/images/SocialIconInstagram.vue'
import SocialIconFacebook from '@/components/images/SocialIconFacebook.vue'
import SocialIconEmail from '@/components/images/SocialIconEmail.vue'
</script>

<template>
  <div class="fitted-container">
    <div id="contact" class="anchor"></div>
    <AnimateOnScroll animation-class="animate-on-scroll-from-left">
      <div class="anchor-container">
        <AnchorHeader :index="4" anchor="contact" title="Contact"/>
      </div>
    </AnimateOnScroll>
    <AnimateOnScroll animation-class="animate-on-scroll-from-bottom">
      <div class="contact-container">
        <div class="contact-description">
          <h3 class="contact-header">
            Available for select freelance opportunities.
          </h3>
          <p class="contact-content">
            Have an exciting project you need help with?
          </p>
          <p class="contact-content">
            Send me an email or contact me via direct message!
          </p>
        </div>
        <div class="contact-links">
          <a href="mailto:cameron@hejazi-far.com" target="_blank">
            <SocialIconEmail class="fill"/>
            <span class="label">Email</span>
          </a>
          <a href="https://www.linkedin.com/in/cameron-hejazi" target="_blank">
            <SocialIconLinkedIn/>
            <span class="label">LinkedIn</span>
          </a>
          <a href="https://www.instagram.com/cameronhejazi" target="_blank">
            <SocialIconInstagram/>
            <span class="label">Instagram</span>
          </a>
          <a href="https://www.facebook.com/cameron7113" target="_blank">
            <SocialIconFacebook/>
            <span class="label">Facebook</span>
          </a>
        </div>
      </div>
    </AnimateOnScroll>
  </div>
</template>

<script>
export default {
  name: 'ContactView'
}
</script>

<style scoped>
.fitted-container {
  padding-top: 128px;
  padding-bottom: 64px;
}

.anchor-container {
  display: block;
  width: 720px;
  max-width: 90%;
  margin: 0 auto;
}

.contact-container {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: center;
  flex-wrap: nowrap;
  width: 720px;
  max-width: 90%;
  margin: 40px auto;
}

.contact-description {
  flex-grow: 1;
  padding-right: 40px;
}

.contact-header {
  display: block;
  margin: 0;
  padding: 0;
  font-size: 24px;
  font-weight: bold;
  color: var(--color-secondary);
}

.contact-content {
  display: block;
  margin: 0;
  padding: 20px 0 0 0;
  font-size: 18px;
  color: var(--color-text-75);
}

.contact-links {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  justify-content: flex-start;
  flex-wrap: nowrap;
}

.contact-links a {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  flex-shrink: 1;
  padding: 8px 16px;
  margin-bottom: 16px;
  font-size: 16px;
  color: var(--color-primary);
  border: 1px solid var(--color-primary);
  border-radius: 5px;
  text-align: center;
  font-weight: bold;
  text-decoration: none;
  outline: none;
  transition: color 250ms ease-in-out, background-color 250ms ease-in-out, border 250ms ease-in-out, padding 250ms ease-in-out, box-shadow 250ms ease-in-out;
}

.contact-links a:hover {
  background-color: var(--color-primary-15);
  border: 3px solid var(--color-primary);
  box-shadow: 0 0 15px var(--color-primary);
  padding: 6px 14px;
}

.contact-links a:active {
  background-color: var(--color-primary-25);
}

.contact-links a:focus:not(:hover):not(:active) {
  border: 1px dashed var(--color-primary);
}

.contact-links a svg {
  width: 28px;
  height: 28px;
}

.contact-links a svg.fill {
  fill: var(--color-primary);
}

.contact-links a .label {
  margin-left: 16px;
}

@media (max-width: 768px) {
  .contact-container {
    flex-direction: column;
  }

  .contact-description {
    padding-right: 0;
  }

  .contact-links {
    margin-top: 40px;
    flex-direction: row;
    flex-wrap: wrap;
  }

  .contact-links a {
    flex-basis: calc(50% - 10px);
    margin: 5px;
  }
}
</style>
