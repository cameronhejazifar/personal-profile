<script setup>
import AnimateOnScroll from '@/components/AnimateOnScroll.vue'
import CorpIconUHIN from '@/components/images/CorpIconUHIN.vue'
import CorpIconBalance from '@/components/images/CorpIconBalance.vue'
import CorpIconFootprints from '@/components/images/CorpIconFootprints.vue'
import TagP from '@/components/TagP.vue'
import TagH6 from '@/components/TagH6.vue'
</script>

<template>
  <div class="employment-history-container">
    <AnimateOnScroll class="card" animationClass="animate-on-scroll-from-left">
      <CorpIconBalance class="corp-logo balance"/>
      <TagH6 class="card-subtitle">
        Co-Founder &amp; Head of Software Development
      </TagH6>
      <a href="https://balancemoney.com" target="_blank" class="corp-link">balancemoney.com</a>
      <TagP class="card-content">
        <p>December, 2021 &mdash; Present</p>
        <p>
          &bull; Co-founded Balance Technologies – a company designed to revolutionize
          digital banking and personal money management.
        </p>
        <p>
          &bull; Responsible for leading the development of the cross-platform
          Balance Money mobile application (iOS and Android).
        </p>
        <p>
          &bull; Integration of various fin-tech vendors including payment processors, card
          issuers, sponsoring banks, etc. using a Laravel-based microservice architecture.
        </p>
      </TagP>
    </AnimateOnScroll>
    <AnimateOnScroll class="card" animationClass="animate-on-scroll-from-bottom">
      <CorpIconUHIN class="corp-logo uhin"/>
      <TagH6 class="card-subtitle">
        Principle Software Engineer
      </TagH6>
      <a href="https://uhin.org" target="_blank" class="corp-link">uhin.org</a>
      <TagP class="card-content">
        <p>March, 2017 &mdash; December, 2021</p>
        <p>
          &bull; Created and maintained the UHIN subscription-based web application
          software suite containing multiple healthcare products used by the industry.
        </p>
        <p>
          &bull; Lead a team responsible for processing and transmitting health care data
          including claims, eligibility & clinical information.
        </p>
        <p>
          &bull; Developed and maintained an alerting system responsible for delivering
          real-time patient payloads to thousands of clinics throughout Utah.
        </p>
      </TagP>
    </AnimateOnScroll>
    <AnimateOnScroll class="card" animationClass="animate-on-scroll-from-right">
      <CorpIconFootprints class="corp-logo footprints"/>
      <TagH6 class="card-subtitle">
        Software Developer
      </TagH6>
      <a href="https://footprints-inc.com" target="_blank" class="corp-link">footprints-inc.com</a>
      <TagP class="card-content">
        <p>June, 2012 - May, 2015</p>
        <p>
          &bull; Among other smaller projects, primarily lead the development of an
          enterprise web application that allowed simultaneous collaboration of
          airplane engineering change management between hundreds of employees
          at Boeing.
        </p>
        <p>
          &bull; Developed custom software solutions for various clients ranging from
          Fortune 100 companies to smaller local Utah based businesses.
        </p>
      </TagP>
    </AnimateOnScroll>
  </div>
</template>

<script>
export default {
  name: 'EmploymentHistoryCards'
}
</script>

<style scoped>
.employment-history-container {
  display: flex;
  flex-direction: row;
  align-items: stretch;
  justify-content: stretch;
  flex-wrap: nowrap;
  padding: 20px;
  margin-top: 30px;
}

.employment-history-container .card {
  display: block;
  flex-basis: calc(33.33333% - 40px);
  flex-grow: 1;
  margin: 20px;
  border-radius: 15px;
  background: transparent;
  border: 3px solid var(--color-secondary-25);
  cursor: default;
  transition: background 250ms ease-in-out, box-shadow 250ms ease-in-out, border 250ms ease-in-out;
}

.employment-history-container .card:hover {
  background: var(--color-secondary-15);
  box-shadow: 0 0 15px var(--color-secondary);
  border-color: var(--color-secondary);
}

.corp-logo {
  display: block;
  width: auto;
  height: 56px;
  margin: 40px 40px 20px 40px;
  object-fit: contain;
}

.corp-logo.footprints {
  height: 128px;
  margin-bottom: 5px;
}

.corp-logo {
  fill: var(--color-secondary);
}

.card-content {
  margin: 0 20px 60px 40px;
}

.card-subtitle {
  margin: 50px 20px 30px 40px;
}

.corp-link {
  display: inline-block;
  margin: 20px;
  font-size: 16px;
  color: var(--color-primary);
  text-decoration: none;
  outline: none;
  border: none;
  border-radius: 2px;
  text-align: center;
  transition: color 250ms ease-in-out, transform 250ms ease-in-out;
}

.corp-link:hover {
  color: var(--color-primary-alt);
  transform: scale(1.05);
}

.corp-link:focus:not(:active):not(:hover) {
  outline: 1px dashed var(--color-primary);
}

@media (max-width: 768px) {
  .employment-history-container {
    flex-direction: column;
    padding: 10px;
  }

  .employment-history-container .card {
    flex-basis: auto;
  }
}
</style>