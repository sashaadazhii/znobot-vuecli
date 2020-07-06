<template>
  <div>
    <main>
      <section>
        <div class="container">
          <div class="heading">
            <div class="heading__title">привіт!</div>
            <div class="heading__subtitle">
              Ми студенти
              <a
                href="https://beetroot.academy/"
                target="blank"
                style="color: #94ceb9;"
              >“Beetroot Academy”</a>
            </div>
          </div>
        </div>
        <div style="text-align: center;">
          <img src="../assets/img/beetroot.png" alt="beetroot" />
        </div>

        <div class="btn-wrapper">
          <router-link to="/" class="btn btn--menu">повернутися</router-link>
        </div>
        <div class="heading__subtitle">To be continued...</div>
      </section>
    </main>
  </div>
</template>
<style scoped>
.container {
  padding: 50px 15px;
}

.btn-wrapper {
  display: flex;
  justify-content: center;
  padding: 30px;
}
.heading__subtitle {
  text-align: center;
}
</style>
