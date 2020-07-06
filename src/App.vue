<template>
  <div id="app">
    <transition name="fade" mode="out-in">
      <router-view />
    </transition>
  </div>
</template>

<style lang="scss">
@import "assets/css/style.css";
@import "assets/css/landscape.css";
@import url("https://fonts.googleapis.com/css?family=Fira+Sans&display=swap");

.fade-enter-active {
  animation: moveUP 0.4nps ease-out;
  opacity: 0;
}

.fade-leave-active {
  animation: going 0.4s ease-out;
}

@keyframes moveUP {
  from {
    transform: translateY(-20px);
    opacity: 0;
  }
  to {
    transform: translateY(0px);
    opacity: 1;
  }
}

@keyframes going {
  from {
    transform: translateY(0px);
  }
  to {
    transform: translateY(-20px);
    opacity: 0;
  }
}
</style>
