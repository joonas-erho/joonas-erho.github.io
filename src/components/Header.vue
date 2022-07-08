<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <div class="header">
    <div>
      <p>Joonas Erho</p>
    </div>
    <div>{{ t('about-me') }}</div>
    <div>{{ t('my-projects') }}</div>
    <div>{{ t('cv') }}</div>
  </div>
</template>

<style scoped lang="scss">
.header {
  background-color: black;
  height: 5em;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 0 7em;

  :first-child {
    flex-grow: 3;
  }

  :not(:first-child) {
    flex-grow: 1;
  }
}
</style>
