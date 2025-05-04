<script setup>
import NewButton from '../components/NewButton.vue'
import WebIcon from '@/assets/web-icon.svg'
import GithubIcon from '@/assets/github-icon.svg'

defineProps({
  image: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  siteLink: {
    type: String,
    required: true,
  },
  gitLink: {
    type: String,
    required: true,
  },
  color: {
    type: String,
    required: true,
  },
})
</script>
<template>
  <div class="project__card">
    <div class="project__visual">
      <img class="project__image" :src="image" />
    </div>
    <div class="project__details">
      <h3 class="project__title">{{ title }}</h3>
      <p class="project__description">{{ description }}</p>
      <div class="project__actions">
        <NewButton :icon="GithubIcon" text="Github" color="black" :link="gitLink" />
        <NewButton :icon="WebIcon" text="Live Site" color="#2F8DDA" :link="siteLink" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.project__card {
  border-radius: 24px;
  overflow: hidden;
  border: 1px solid #d9d9d9;
}
.project__visual {
  height: 250px;
  background-color: v-bind('color');
  padding: 1rem;
  text-align: center;
}

.project__image {
  height: 100%;
  margin-bottom: -2rem;
}

.project__details {
  padding: 1rem;
}

.project__title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.8rem;
}

.project__actions {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
}
</style>
