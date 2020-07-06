<template>
  <div class="header-nav">
    <div class="logo"></div>
    <nav class="menu-wrapper">
      <ul class="menu">
        <li class="menu__item">
          <a
            href="#"
            class="menu__link"
            v-scroll-to="{ element: '#read', duration: 1300 }"
          >як користуватись?</a>
        </li>
        <li class="menu__item">
          <router-link to="/about" class="menu__link">про нас</router-link>
        </li>
      </ul>
      <div class="btn-wrapper">
        <a
          href="#"
          class="btn btn--menu"
          v-scroll-to="{ element: '#bot', duration: 1000 }"
        >вибрати бота</a>
      </div>
    </nav>
  </div>
</template>

<script>
export default {};
</script>
<style scoped>
</style>