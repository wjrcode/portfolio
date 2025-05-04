<script setup>
defineProps({
  icon: {
    type: String,
    required: true,
  },
  text: {
    type: String,
    required: true,
  },
  color: {
    type: String,
    required: true,
  },
  link: {
    type: String,
    required: true,
  },
})

const gotoLink = (link) => {
  window.open(link, '_blank')
}
</script>

<template>
  <button class="button" @click="gotoLink(link)">
    <img class="button__img" :src="icon" alt="icon" />
    {{ text }}
  </button>
</template>

<style scoped>
.button {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 16px;
  border: none;
  border-radius: 0.9rem;
  background-color: v-bind('color');
  color: white;
  font-weight: 600;
}

.button__img {
  width: 20px;
  height: 20px;
}
</style>
