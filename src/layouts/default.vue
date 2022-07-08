<template>
  <main class="text-center text-gray-700 dark:text-gray-200">
    <Header />
    <RouterView class="side-padding" />
  </main>
</template>

<style scoped lang="scss">
.side-padding {
  padding: 8em max(1em, 10vw);
}
</style>
