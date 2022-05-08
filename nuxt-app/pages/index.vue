<template>
  <div class="top-space" />
  <div class="intro-container">
    <div class="avatar-container avatar-anim-class">
      <img src="@/assets/images/avatar.png" alt="Hey it's me!" class="avatar"/>
    </div>
    <div class="intro-text-container intro-text-anim-class">
      <p class="big-title hello-anim-class">
        Hello.
      </p>
      <p class="introduction">
        My name is<br/>Joonas.
      </p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.main-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  align-content: center;
  margin-left: 5vw;
  margin-right: 5vw;
}

.top-space {
  margin-bottom: 30vh;
}

.intro-container {
  display: flex;
  margin: auto;
  width: min(1000px, 90vw);
}

.avatar-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: max(200px, 30vw);
}

.avatar {
  width: 300px;
  height: 300px;
  border-radius: 50%;
}

.intro-text-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  width: max(200px, 30vw);
}

.introduction {
  font-size: 2.5em;
  text-align: end;
}

.hello-anim-class {
  animation-name: hello-anim;
  animation-duration: 1000ms;
  animation-iteration-count: 1;
  animation-timing-function: ease-in-out;
}

@keyframes hello-anim {
  0% {
    opacity: 0;
    transform: translate(0, -1em);
  }
  100% {
    opacity: 1;
    transform: translate(0, 0);
  }
}

.avatar-anim-class {
  animation-name: avatar-anim;
  animation-duration: 1500ms;
  animation-delay: 0ms;
  animation-iteration-count: 1;
  animation-fill-mode: forwards;
}

@keyframes avatar-anim {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>