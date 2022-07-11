<script setup lang="ts">
const props = defineProps<{
  project: {
    name: string
    images: string[]
    years: string
    typeTags: string[]
    techTags: string[]
    shortDesc: string
  }
}>()
</script>

<template>
  <div class="base">
    <NCarousel show-arrow class="carousel-style">
      <img v-for="image in project.images" :key="image" class="carousel-img" :src="image">
    </NCarousel>
    <div class="text-area">
      <p class="title">
        {{ project.name }}
      </p>
      {{ project.years }}
    </div>
  </div>
</template>

<style scoped lang="scss">
.base {
  height: 500px;
  width: 400px;
  background-color: rgb(57, 57, 61);
  box-shadow: 3px 3px 5px #141414;
  border-radius: 10px;
  overflow: hidden;
  text-align: left;
}

.carousel-style {
  height: 225px;
}

.text-area {
  margin: 0.5em;
}

.title {
  text-transform: uppercase;
  font-size: 1.5em;
  font-weight: 600;
}
</style>
