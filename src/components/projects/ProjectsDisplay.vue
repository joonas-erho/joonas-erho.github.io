<script setup lang="ts">
const props = defineProps<{
  showFull: boolean
}>()

const projects = [
  {
    name: 'Bittiliiga Webpage',
    images: ['assets/images/avatar.png'],
    years: '2019-2021',
    typeTags: [
      {
        text: 'Work',
        color: '#be43aa',
      },
      {
        text: 'Solo',
        color: '#be4300',
      },
    ],
    techTags: [
      {
        text: 'Vue.js',
        color: '#be43aa',
      },
      {
        text: 'Nuxt.js',
        color: '#be4300',
      },
    ],
    shortDesc: 'I created and maintained the webpages for Bittiliiga using Vue and Nuxt.js.',
  },
  {
    name: 'Bittiliiga Platform',
    images: ['assets/images/avatar.png'],
    years: '2019-2022',
    typeTags: [
      {
        text: 'Work',
        color: '#be43aa',
      },
      {
        text: 'As a team',
        color: '#be4300',
      },
    ],
    techTags: [
      {
        text: 'Vue.js',
        color: '#be43aa',
      },
      {
        text: 'Nuxt.js',
        color: '#be4300',
      },
    ],
    shortDesc: 'I worked on the Bittiliiga game platform as a part of team, working mainly on the front-end of the platform.',
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
