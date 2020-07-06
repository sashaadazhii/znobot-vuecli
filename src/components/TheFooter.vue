<template>
  <footer>
    <section class="footer-nav">
      <div class="container">
        <div class="footer-menu-wrapper">
          <nav class="menu-wrapper">
            <ul class="menu">
              <li class="menu__item">
                <a
                  href="#"
                  class="menu__link"
                  v-scroll-to="{ element: '#read', duration: 800 }"
                >як користуватись?</a>
              </li>
              <li class="menu__item">
                <router-link to="/about" class="menu__link">про нас</router-link>
              </li>
            </ul>
            <div class="btn-wrapper">
              <a
                href="#"
                class="btn btn--light"
                v-scroll-to="{ element: '#bot', duration: 1000 }"
              >вибрати бота</a>
            </div>
          </nav>

          <router-link to @click.native="scrollToTop" class="btn btn--light btn--top">
            <svg
              width="16"
              height="9"
              viewBox="0 0 16 9"
              fill="#278BFF"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M8.70711 0.292893C8.31658 -0.097631 7.68342 -0.097631 7.29289 0.292893L0.928932 6.65685C0.538408 7.04738 0.538408 7.68054 0.928932 8.07107C1.31946 8.46159 1.95262 8.46159 2.34315 8.07107L8 2.41421L13.6569 8.07107C14.0474 8.46159 14.6805 8.46159 15.0711 8.07107C15.4616 7.68054 15.4616 7.04738 15.0711 6.65685L8.70711 0.292893ZM9 2V1L7 1V2L9 2Z"
                fill="#288BFF"
              />
            </svg>
          </router-link>
        </div>
      </div>
      <!-- </div> -->
    </section>

    <section class="footer-copyright">
      <div class="container">
        <div class="copyright">Всі права захищено © 2019</div>
      </div>
    </section>
  </footer>
</template>
<script>
export default {
  methods: {
    scrollToTop() {
      window.scroll({
        top: 0,
        left: 0,
        behavior: "smooth"
      });
    }
  }
};
</script>
<style scoped>
</style>