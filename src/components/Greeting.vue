<template>
  <NGrid :cols="2">
    <NGridItem>
      <NAvatar :size="300" round src="/assets/images/avatar.png" />
    </NGridItem>
    <NGridItem class="text-container">
      <p class="greeting-text">
        Hi, my name is Joonas.
      </p>
      <p class="subtext">
        I am an aspiring computer science student and software developer from Finland.
      </p>
    </NGridItem>
  </NGrid>
</template>

<style scoped lang="scss">
.text-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.greeting-text {
  font-size: 4em;
  font-weight: 600;
}

.subtext {
  font-size: 1.1em;
  opacity: 0.6;
}
</style>
