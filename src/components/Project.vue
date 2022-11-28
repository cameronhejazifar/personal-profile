<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue'
import ExternalLinkIcon from '@/components/images/ExternalLinkIcon.vue'
import TagP from '@/components/TagP.vue'
</script>

<template>
  <div class="project">
    <AnimateOnScroll :animation-class="even ? 'animate-on-scroll-from-left' : 'animate-on-scroll-from-right'"
                     class="animator-container">
      <div :class="{'preview-container': true, 'even': even, 'odd': !even}">
        <div class="preview-actions">
          <span></span>
          <span></span>
          <span></span>
        </div>
        <slot name="image"/>
      </div>
    </AnimateOnScroll>
    <AnimateOnScroll :animation-class="even ? 'animate-on-scroll-from-right' : 'animate-on-scroll-from-left'"
                     class="animator-container">
      <div :class="{'info-container': true, 'even': even, 'odd': !even}">
        <h4 :class="{'project-name': true, 'even': even, 'odd': !even}">{{ projectName }}</h4>
        <h6 :class="{'platform': true, 'even': even, 'odd': !even}">{{ platform }}</h6>
        <div :class="{'description': true, 'even': even, 'odd': !even}">
          <TagP>
            <slot/>
          </TagP>
        </div>
        <div :class="{'links': true, 'even': even, 'odd': !even}" v-if="links.length > 0">
          <a v-for="link in links" :href="link.url" target="_blank">
            <span class="text">{{ link.label }}</span>
            <ExternalLinkIcon class="icon"></ExternalLinkIcon>
          </a>
        </div>
      </div>
    </AnimateOnScroll>
  </div>
</template>

<script>
export default {
  name: 'Project',
  props: {
    even: {
      type: Boolean,
      required: true
    },
    projectName: {
      type: String,
      required: true
    },
    platform: {
      type: String,
      required: true
    },
    links: {
      type: Array,
      default: []
    }
  }
}
</script>

<style scoped>
.project {
  margin: 32px auto;
  display: block;
  position: relative;
  width: 960px;
  max-width: 90%;
  min-height: 520px;
}

.animator-container {
  position: absolute;
  display: block;
  min-height: 520px;
  width: 100%;
}

.info-container {
  position: absolute;
  display: block;
  top: 50%;
  transform: translateY(-50%);
}

.info-container.even {
  right: 0;
}

.info-container.odd {
  left: 0;
}

.project-name {
  display: block;
  padding: 0;
  color: var(--color-secondary);
  font-size: 22px;
  font-weight: bold;
}

.project-name.even {
  margin: 0 5px 0 0;
  text-align: right;
}

.project-name.odd {
  margin: 0 0 0 5px;
  text-align: left;
}

.platform {
  display: block;
  padding: 0;
  color: var(--color-text-90);
  font-size: 14px;
  font-weight: normal;
  text-transform: uppercase;
}

.platform.even {
  margin: 2px 5px 0 0;
  text-align: right;
}

.platform.odd {
  margin: 2px 0 0 5px;
  text-align: left;
}

.description {
  display: block;
  width: auto;
  height: auto;
  padding: 10px 10px 20px 35px;
  color: var(--color-text-75);
  background: var(--color-background-90);
  border: 2px solid var(--color-secondary-15);
  border-radius: 10px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, .15);
}

.description.even {
  margin: 15px 0 15px 25%;
}

.description.odd {
  margin: 15px 25% 15px 0;
}

.links {
  display: flex;
  flex-direction: row;
  align-items: center;
  flex-wrap: nowrap;
}

.links.even {
  justify-content: flex-end;
  margin: 0 5px 0 0;
}

.links.odd {
  justify-content: flex-start;
  margin: 0 0 0 5px;
}

.links a {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  flex-wrap: nowrap;
  flex-shrink: 1;
  font-size: 16px;
  color: var(--color-primary);
  border-radius: 2px;
  border: none;
  text-decoration: none;
  outline: none;
  transition: color 250ms ease-in-out, transform 250ms ease-in-out;
}

.links a:hover {
  color: var(--color-primary-alt);
  transform: scale(1.05);
}

.links a:focus:not(:active):not(:hover) {
  outline: 1px dashed var(--color-primary);
}

.links.even a {
  margin-left: 15px;
}

.links.odd a {
  margin-right: 15px;
}

.links a .icon {
  margin-left: 10px;
  width: 22px;
  height: 22px;
}

.preview-container {
  position: absolute;
  display: block;
  top: 50%;
  margin-top: -260px;
  width: 65%;
  height: 520px;
  border-radius: 15px;
  padding: 45px 15px 15px 15px;
  outline: 3px solid var(--color-secondary-25);
  overflow: visible;
  opacity: 0.5;
  transition: opacity 250ms ease-in-out;
}

.project:hover .preview-container {
  opacity: 0.75;
}

.preview-container.even {
  left: 0;
  transform: perspective(800px) rotateY(25deg) scale(.8) rotateX(10deg);
}

.preview-container.odd {
  right: 0;
  transform: perspective(800px) rotateY(-25deg) scale(.8) rotateX(10deg);
}

.preview-actions {
  position: absolute;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  flex-wrap: nowrap;
  left: 15px;
  top: 15px;
  width: 65px;
  height: 20px;
}

.preview-actions span {
  display: block;
  width: 15px;
  height: 15px;
  border-radius: 8px;
  opacity: 0.5;
}

.preview-actions span:nth-child(1) {
  background: #ec6a5e;
}

.preview-actions span:nth-child(2) {
  background: #f3bf4f;
}

.preview-actions span:nth-child(3) {
  background: #61c555;
}

@media (max-width: 768px) {
  .project {
    margin: 64px auto 32px auto;
  }

  .preview-container.even, .preview-container.odd {
    transform: none;
    width: 100%;
    height: 480px;
  }

  .preview-container, .project:hover .preview-container {
    opacity: 0.075;
  }

  .info-container.even, .info-container.odd {
    padding: 0 20px 20px 20px;
    left: 0;
    right: auto;
  }

  .project-name.even, .project-name.odd {
    margin: 0;
    text-align: left;
  }

  .platform {
    display: none;
  }

  .description.even, .description.odd {
    color: var(--color-text-90);
    background: transparent;
    border: none;
    border-radius: 0;
    box-shadow: none;
    margin: 15px 0;
    padding: 10px 10px 10px 20px;
    text-align: left;
  }

  .links.even, .links.odd {
    justify-content: flex-start;
    margin: 0;
  }

  .links.even a, .links.odd a {
    margin: 0;
  }

}
</style>
