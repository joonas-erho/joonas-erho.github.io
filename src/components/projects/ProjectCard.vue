<script setup lang="ts">
const props = defineProps<{
  project: {
    name: string
    images: string[]
    years: string
    typeTags: {
      text: string
      color: string }[]
    techTags: {
      text: string
      color: string }[]
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
      <div class="type-chips">
        <Chip :text="project.years" color="#242543" />
        <Chip v-for="type in project.typeTags" :key="type.text" :text="type.text" :color="type.color" />
      </div>
      <p class="short-desc">
        {{ project.shortDesc }}
      </p>
      <div class="type-chips">
        <Chip v-for="tech in project.techTags" :key="tech.text" :text="tech.text" :color="tech.color" />
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.base {
  height: 450px;
  width: 400px;
  background-color: rgb(57, 57, 61);
  box-shadow: 3px 3px 5px #141414;
  border-radius: 10px;
  overflow: hidden;
  text-align: left;
}

.carousel-style {
  height: 200px;
}

.text-area {
  margin: 0.5em;
}

.title {
  font-size: 2em;
  font-weight: 600;
  margin-left: 0.1em;
}

.type-chips {
  margin-top: 0.2em;

  * {
    margin-right: 5px;
  }
}

.short-desc {
  margin-left: 0.2em;
  margin-top: 0.75em;
  font-size: 1.1em;
}
</style>
