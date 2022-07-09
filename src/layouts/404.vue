<script setup lang="ts">
const router = useRouter()
const { t } = useI18n()
</script>

<template>
  <main class="text-center text-gray-700 dark:text-gray-200">
    <Header />
    <div text-4xl mt-25>
      <div i-carbon-warning inline-block />
    </div>
    <RouterView />
    <div>
      <button btn text-sm m="3 t8" @click="router.back()">
        {{ t('button.back') }}
      </button>
    </div>
    <Footer />
  </main>
</template>
