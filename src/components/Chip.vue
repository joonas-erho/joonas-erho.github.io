<script setup lang="ts">
const props = defineProps<{
  text: string
  color: string
}>()
</script>

<template>
  <div class="chip" :style="`background-color:${color}` ">
    {{ text }}
  </div>
</template>

<style scoped lang="scss">
.chip {
  border-radius: 20px;
  display: inline-block;
  padding: 0.25em 0.75em;
}
</style>
