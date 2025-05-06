<script setup>
import NewButton from './components/NewButton.vue'
import GithubIcon from '@/assets/github-icon.svg'
import LinkedinIcon from '@/assets/linkedin-icon.png'
import EmailIcon from '@/assets/email-icon.svg'
import ProjectCard from './components/ProjectCard.vue'
</script>

<template>
  <header class="header">
    <div class="header__texts">
      <p class="header__span">Olá! I'm</p>
      <h1 class="header__tittle">Willian Pinheiro Jr</h1>
      <p class="header__description">Full Stack developer from Brazil.</p>
      <div class="header__links">
        <NewButton
          :icon="GithubIcon"
          text="Github"
          color="black"
          link="https://github.com/wjrcode"
        />
        <NewButton
          :icon="LinkedinIcon"
          text="LinkedIn"
          color="#0E76A8"
          link="https://github.com/wjrcode"
        />
        <NewButton :icon="EmailIcon" text="" color="#DA2F32" link="https://github.com/wjrcode" />
      </div>
    </div>
    <img src="" alt="" class="header__image" />
  </header>
  <section class="section">
    <h2 class="section__tittle">Projects</h2>
    <div class="section__list">
      <ProjectCard
        title="Conference ticket generator"
        image="./ticket-generator-screenshot.png"
        description="Challenge from Front-end Mentor; It consists of a form, its validation and a ticket page result; Build only with HTML, CSS and JavaScript"
        gitLink="https://github.com/wjrcode/conference-ticket-generator-main/"
        siteLink="https://wjrcode.github.io/conference-ticket-generator-main/"
        color="#F57463"
      />
      <ProjectCard
        title="Mortgage repayment calculator"
        image="./calculator-screenshot.png"
        description="Challenge from Front-end Mentor; It consists of a form, its validation and a ticket page result; Build only with HTML, CSS and JavaScript"
        gitLink="https://github.com/wjrcode/mortgage-repayment-calculator-main/"
        siteLink="https://wjrcode.github.io/mortgage-repayment-calculator-main/"
        color="#D7F3FF"
      />
    </div>
  </section>
</template>

<style>
:root {
  font-family: 'Roboto', sans-serif;
}

.header {
  display: flex;
}

.header__span {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 3rem;
  line-height: 3.5rem;
}

.header__tittle {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 5rem;
  color: #2f8dda;
  line-height: 5.5rem;
}

.header__links {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
  margin-bottom: 3rem;
}

.section__list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.section__tittle {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2.25rem;
}

@media (min-width: 1024px) {
  .section__list {
    flex-direction: row;
  }
}
</style>
