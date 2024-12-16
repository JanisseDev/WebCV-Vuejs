<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  skills: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div class="main">
    <h2 class="font-title">{{ title }}</h2>
    <p class="font-subtitle" v-for="(skill) in skills">{{ skill }}</p>
  </div>
</template>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.font-title {
  font-weight: 400;
  font-size: 0.9rem;
  letter-spacing: 0.04rem;
  margin-bottom: 8px;
}

.font-subtitle {
  font-weight: 300;
  font-size: 0.8rem;
  font-style: italic;
  letter-spacing: 0rem;
  padding-left: 6px;
}
</style>