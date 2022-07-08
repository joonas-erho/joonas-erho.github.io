<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <div>
    <Greeting class="pt-10" />
    <p class="large-title">
      {{ t('about-me') }}
    </p>
    <p>
      {{ t('short-bio') }}
    </p>
  </div>
</template>
