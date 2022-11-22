<script setup>
import LanguageIconVue from '@/components/images/LanguageIconVue.vue'
import LanguageIconTailwind from '@/components/images/LanguageIconTailwind.vue'
import LanguageIconJQuery from '@/components/images/LanguageIconJQuery.vue'
import LanguageIconBulma from '@/components/images/LanguageIconBulma.vue'
import LanguageIconSass from '@/components/images/LanguageIconSass.vue'
import LanguageIconObjectiveC from '@/components/images/LanguageIconObjectiveC.vue'
import LanguageIconSwift from '@/components/images/LanguageIconSwift.vue'
import LanguageIconJava from '@/components/images/LanguageIconJava.vue'
import LanguageIconKotlin from '@/components/images/LanguageIconKotlin.vue'
import LanguageIconFlutter from '@/components/images/LanguageIconFlutter.vue'
import LanguageIconLaravel from '@/components/images/LanguageIconLaravel.vue'
import LanguageIconMySQL from '@/components/images/LanguageIconMySQL.vue'
import LanguageIconKafka from '@/components/images/LanguageIconKafka.vue'
import LanguageIconRabbitMQ from '@/components/images/LanguageIconRabbitMQ.vue'
import LanguageIconPHP from '@/components/images/LanguageIconPHP.vue'
</script>

<template>
  <div class="languages-container">
    <div class="languages-header">
      <span class="label">Web</span>
      <span class="line"></span>
    </div>
    <div class="language-grid">
      <a href="https://vuejs.org" target="_blank" class="language language-vue">
        <LanguageIconVue class="icon"/>
        <span class="label">Vue.js</span>
      </a>
      <a href="https://tailwindcss.com" target="_blank" class="language language-tailwind">
        <LanguageIconTailwind class="icon"/>
        <span class="label">Tailwind</span>
      </a>
      <a href="https://jquery.com" target="_blank" class="language language-jquery">
        <LanguageIconJQuery class="icon"/>
        <span class="label">jQuery</span>
      </a>
      <a href="https://bulma.io" target="_blank" class="language language-bulma">
        <LanguageIconBulma class="icon"/>
        <span class="label">Bulma</span>
      </a>
      <a href="https://sass-lang.com" target="_blank" class="language language-sass">
        <LanguageIconSass class="icon"/>
        <span class="label">Sass</span>
      </a>
    </div>
    <div class="languages-header">
      <span class="label">Mobile</span>
      <span class="line"></span>
    </div>
    <div class="language-grid">
      <a href="https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html"
         target="_blank" class="language language-objective-c">
        <LanguageIconObjectiveC class="icon"/>
        <span class="label">Objective-C</span>
      </a>
      <a href="https://docs.swift.org/swift-book" target="_blank" class="language language-swift">
        <LanguageIconSwift class="icon"/>
        <span class="label">Swift</span>
      </a>
      <a href="https://www.java.com/" target="_blank" class="language language-java">
        <LanguageIconJava class="icon"/>
        <span class="label">Java</span>
      </a>
      <a href="https://kotlinlang.org/" target="_blank" class="language language-kotlin">
        <LanguageIconKotlin class="icon"/>
        <span class="label">Kotlin</span>
      </a>
      <a href="https://flutter.dev/" target="_blank" class="language language-flutter">
        <LanguageIconFlutter class="icon"/>
        <span class="label">Flutter</span>
      </a>
    </div>
    <div class="languages-header">
      <span class="label">Backend</span>
      <span class="line"></span>
    </div>
    <div class="language-grid">
      <a href="https://laravel.com" target="_blank" class="language language-laravel">
        <LanguageIconLaravel class="icon"/>
        <span class="label">Laravel</span>
      </a>
      <a href="https://www.mysql.com" target="_blank" class="language language-mysql">
        <LanguageIconMySQL class="icon"/>
        <span class="label">MySQL</span>
      </a>
      <a href="https://kafka.apache.org" target="_blank" class="language language-kafka">
        <LanguageIconKafka class="icon"/>
        <span class="label">Kafka</span>
      </a>
      <a href="https://www.rabbitmq.com" target="_blank" class="language language-rabbit-mq">
        <LanguageIconRabbitMQ class="icon"/>
        <span class="label">RabbitMQ</span>
      </a>
      <a href="https://www.php.net" target="_blank" class="language language-php">
        <LanguageIconPHP class="icon"/>
        <span class="label">PHP</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProgrammingLanguagesGrid'
}
</script>

<style scoped>
.languages-container {
  display: block;
  width: 810px;
  max-width: 90%;
  margin: 128px auto 0 auto;
  background: var(--color-secondary-75);
  border-radius: 15px;
  padding: 5px;
}

.languages-header {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  flex-wrap: nowrap;
  padding: 30px 5px 0 5px;
}

.languages-header:first-child {
  padding-top: 10px;
}

.languages-header .label {
  font-size: 18px;
  color: var(--color-background);
  font-weight: bold;
}

.languages-header .line {
  display: block;
  flex-grow: 1;
  height: 3px;
  margin-left: 10px;
  background: var(--color-background-25);
}

.language-grid {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  flex-wrap: nowrap;
}

.language {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  flex-grow: 1;
  margin: 5px;
  background: var(--color-background-75);
  border-radius: 10px;
  text-decoration: none;
  outline: none;
  border: none;
  transition: background 250ms ease-in-out, transform 250ms ease-in-out;
}

.language:hover {
  background: var(--color-background);
  animation: effect linear 750ms;
}

.language:focus:not(:active):not(:hover) {
  outline: 1px dashed var(--color-primary-alt);
}

@keyframes effect {
  from {
    transform: scale3d(1, 1, 1);
  }

  30% {
    transform: scale3d(0.75, 1.5, 1);
  }

  40% {
    transform: scale3d(1.25, 0.75, 1);
  }

  50% {
    transform: scale3d(0.85, 1.35, 1);
  }

  65% {
    transform: scale3d(1.05, .95, 1);
  }

  75% {
    transform: scale3d(.95, 1.2, 1);
  }

  to {
    transform: scale3d(1, 1, 1);
  }
}

.language .label {
  flex-grow: 1;
  font-size: 14px;
  color: var(--color-secondary);
  font-weight: bold;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.language .icon {
  display: block;
  width: 28px;
  height: 28px;
  margin: 10px;
}

.language-vue .icon {
  fill: var(--color-secondary);
}

.language-tailwind .icon {
  stroke: var(--color-secondary);
}

.language-jquery .icon {
  fill: var(--color-secondary);
}

.language-bulma .icon {
  fill: var(--color-secondary);
}

.language-sass .icon {
  fill: var(--color-secondary);
}

.language-objective-c .icon {
  stroke: var(--color-secondary);
}

.language-swift .icon {
  stroke: var(--color-secondary);
}

.language-java .icon {
  fill: var(--color-secondary);
}

.language-kotlin .icon {
  stroke: var(--color-secondary);
}

.language-flutter .icon {
  fill: var(--color-secondary);
}

.language-laravel .icon {
  fill: var(--color-secondary);
}

.language-mysql .icon {
  stroke: var(--color-secondary);
}

.language-kafka .icon {
  fill: var(--color-secondary);
}

.language-rabbit-mq .icon {
  fill: var(--color-secondary);
}

.language-php .icon {
  fill: var(--color-secondary);
}

@media (max-width: 768px) {
  .language-grid {
    flex-direction: row;
    flex-wrap: wrap;
    align-items: stretch;
  }

  .language {
    flex-basis: calc(50% - 10px);
  }
}
</style>
