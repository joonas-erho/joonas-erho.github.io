<script setup lang="ts">
const props = defineProps<{
  showFull: boolean
}>()

const projects = [
  {
    name: 'Bittiliiga Webpage',
    images: ['assets/images/avatar.png'],
    years: '2019-2021',
    typeTags: ['Work', 'With a team'],
    techTags: ['Vue.js', 'Nuxt.js'],
    shortDesc: 'I did stuff!',
  },
  {
    name: 'Bittiliiga Platform',
    images: ['assets/images/avatar.png'],
    years: '2019-2022',
    typeTags: ['Work', 'With a team'],
    techTags: ['Vue.js', 'Nuxt.js'],
    shortDesc: 'I did stuff!',
  },
]
</script>

<template>
  <div class="card-container">
    <ProjectCard v-for="project in projects" :key="project.name" :project="project" />
  </div>
</template>

<style scoped lang="scss">
.card-container {
  display: flex;
  gap: 1em;
}
</style>
