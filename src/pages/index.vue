<script setup lang="ts">
const { t } = useI18n()
const router = useRouter()
</script>

<template>
  <div>
    <Greeting class="pt-10" />
    <div class="sect">
      <p class="large-title">
        {{ t('about-me') }}
      </p>
      <p>
        {{ t('short-bio') }}
      </p>
      <p>
        {{ t('short-bio-b') }}
      </p>
    </div>
    <div class="sect">
      <p class="large-title">
        {{ t('my-projects') }}
      </p>
      <ProjectsDisplay :show-full="false" />
    </div>
    <div class="sect">
      <p class="large-title">
        {{ t('cv') }}
      </p>
      <NButton type="primary" class="link-button" @click="router.push('/cv')">
        {{ t('cv-button') }}
        <div i-carbon-arrow-right class="ml-3 -mr-2" />
      </NButton>
    </div>
  </div>
</template>

<style scoped lang="scss">
.sect {
  margin-top: 2em;
  max-width: $max-width;
  margin: auto;

  p {
    margin-top: 2em;
  }
}
</style>
