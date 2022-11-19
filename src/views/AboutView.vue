<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue';
import TagH2 from '@/components/TagH2.vue';
import TagP from '@/components/TagP.vue';
import TagBody from '@/components/TagBody.vue';
import TypewriterText from '@/components/TypewriterText.vue';
</script>

<template>
  <div id="about" class="fitted-container">
    <AnimateOnScroll animation-class="animate-on-scroll-from-left">
      <TagBody class="about-text">
        <TagH2 class="name">
          <TypewriterText>Cameron Hejazi-Far</TypewriterText>
        </TagH2>
        <TagP class="description">
          <p class="occupation">Full-Stack Developer</p>
          <!-- TODO: replace placeholder "About Me" content here -->
          <p>
            Highly motivated lead software engineer with 10+ years of experience in full-stack
            development and all phases of the software development lifecycle.
          </p>
          <p>
            Well-versed in many areas including web & mobile application development, database
            design, event streaming, and creating/maintaining RESTful APIs.
          </p>
        </TagP>
      </TagBody>
    </AnimateOnScroll>
    <AnimateOnScroll animation-class="animate-on-scroll-from-right">
      <div class="profile-picture"></div>
    </AnimateOnScroll>
  </div>
</template>

<script>
export default {
  name: 'AboutView',

}
</script>

<style scoped>
.fitted-container {
  max-width: calc(var(--dimension-max-screen-width) * 0.75);
  min-height: 100vh;
  padding-top: var(--dimension-header-height) !important;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.about-text {
  margin: 40px 80px 40px 40px;
}

.name {
  color: var(--color-secondary);
}

.occupation {
  font-size: 1.25rem;
  color: var(--color-text);
}

.description {
}

.profile-picture {
  display: block;
  position: relative;
  width: 300px;
  height: 300px;
  background: transparent url("@/assets/profile-picture.jpg") no-repeat 0 0;
  background-size: contain;
  border-radius: 10px;
  border: 2px solid var(--color-secondary);
  margin-right: 40px;
}

.profile-picture::after {
  content: "";
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  top: 15px;
  left: 15px;
  border-radius: 10px;
  border: 2px solid var(--color-secondary);
  z-index: -1;
}

.profile-picture:hover, .profile-picture:hover::after {
  border-color: var(--color-primary);
}

@media (max-width: 768px) {
  .name {
    font-size: 2rem;
  }

  .occupation {
    font-size: 1rem;
  }

  .description {
    font-size: 0.9rem;
  }

  .fitted-container {
    flex-direction: column;
  }

  .about-text {
    margin-right: 40px;
    margin-bottom: 120px;
  }
}
</style>
