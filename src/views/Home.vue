<template>
  <div>
    <header class="header">
      <section class="main-header">
        <div class="container">
          <MainNav />
          <div class="header-content">
            <div class="slogan">
              <div class="slogan__title">
                Я уже користуюсь ЗНО ботом,
                <span class="accent-text">а ти?</span>
              </div>
              <div class="slogan__subtitle">
                Не хочеш аби тебе послали в
                заслання? тоді мерщій проходити тести!
              </div>
            </div>
            <div class="btn-wrapper">
              <a
                href="#"
                class="btn btn--big"
                v-scroll-to="{ element: '#bot', duration: 900 }"
              >вибрати бота</a>
            </div>
            <div class="btn-wrapper">
              <a
                href="#"
                class="btn btn--big btn--transparent"
                v-scroll-to="{ element: '#read', duration: 1100 }"
              >як користуватись?</a>
            </div>
          </div>
        </div>
      </section>
    </header>

    <main>
      <section class="random">
        <div class="container">
          <div class="heading">
            <div class="heading__title">сектор приз від Андрійовича</div>
          </div>
          <div class="test-wrapper">
            <div class="heading__subtitle-wrapper">
              <div class="heading__subtitle">Я офігів від питання, а ти дай відповідь:</div>
              <div class="heading__img">
                <img src="../assets/img/symonenko.png" alt="question picture" class="heading__pic" />
              </div>
            </div>
            <Test />
          </div>
        </div>
      </section>

      <section class="main-items" id="bot">
        <div class="container">
          <div class="heading">
            <div class="heading__title">вибери бота</div>
          </div>
          <ul class="list">
            <li class="list__item list__item--main">
              <div class="item-container">
                <div class="item-image-container">
                  <div class="item-visible">
                    <img src="../assets/img/shevchenko.jpg" class="list__img" alt="lang" />
                  </div>
                  <SocialLinks />
                  <div class="item-title-container">
                    <h4 class="list__title">Українська мова та література</h4>
                  </div>
                  <div class="shadow"></div>
                </div>
              </div>
            </li>
            <li class="list__item">
              <div class="item-container">
                <div class="item-image-container">
                  <div class="item-visible">
                    <img src="../assets/img/khmelnytskyi_small.jpg" class="list__img" alt="history" />
                  </div>
                  <SocialLinks />
                  <div class="item-title-container">
                    <h4 class="list__title">історія України</h4>
                  </div>
                  <div class="shadow"></div>
                </div>
              </div>
            </li>
            <li class="list__item">
              <div class="item-container">
                <div class="item-image-container">
                  <div class="item-visible">
                    <img src="../assets/img/pythagoras_small.jpg" class="list__img" alt="math" />
                  </div>
                  <SocialLinks />
                  <div class="item-title-container">
                    <h4 class="list__title">Математика</h4>
                  </div>
                  <div class="shadow"></div>
                </div>
              </div>
            </li>
            <li class="list__item">
              <div class="item-container">
                <div class="item-image-container">
                  <div class="item-visible">
                    <img src="../assets/img/vernadskiy_small.jpg" class="list__img" alt="geography" />
                  </div>
                  <SocialLinks />
                  <div class="item-title-container">
                    <h4 class="list__title">Географія</h4>
                  </div>
                  <div class="shadow"></div>
                </div>
              </div>
            </li>
            <li class="list__item">
              <div class="item-container">
                <div class="item-image-container">
                  <div class="item-visible">
                    <img src="../assets/img/tesla_small.jpg" class="list__img" alt="physics" />
                  </div>
                  <SocialLinks />
                  <div class="item-title-container">
                    <h4 class="list__title">Хімія</h4>
                  </div>
                  <div class="shadow"></div>
                </div>
              </div>
            </li>
            <li class="list__item">
              <div class="item-container">
                <div class="item-image-container">
                  <div class="item-visible">
                    <img src="../assets/img/kjuri_small.jpg" class="list__img" alt="chemistry" />
                  </div>
                  <SocialLinks />
                  <div class="item-title-container">
                    <h4 class="list__title">Фізика</h4>
                  </div>
                  <div class="shadow"></div>
                </div>
              </div>
            </li>
            <li class="list__item">
              <div class="item-container">
                <div class="item-image-container">
                  <div class="item-visible">
                    <img src="../assets/img/amosov_small.jpg" class="list__img" alt="biology" />
                  </div>
                  <SocialLinks />
                  <div class="item-title-container">
                    <h4 class="list__title">Біологія</h4>
                  </div>
                  <div class="shadow"></div>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </section>

      <section class="instruction" id="read">
        <div class="container">
          <div class="heading">
            <div class="heading__title heading__title--light">як користуватися?</div>
          </div>

          <div class="instr-wrapper">
            <div class="instr-block instr-block--first">
              <div class="instr-block__img">
                <img src="../assets/img/hand1.png" alt="how to use bot" class="instr-block__pic" />
              </div>
              <div class="instr-block__desc">
                <div class="instr-block__text">Береш свій телефон</div>
                <div class="instr-block__number">1</div>
              </div>
            </div>
            <div class="instr-block instr-block--reverse">
              <div class="instr-block__img">
                <img src="../assets/img/hand2.png" alt="how to use bot" class="instr-block__pic" />
              </div>
              <div class="instr-block__desc">
                <div class="instr-block__text">Вибираєш бота</div>
                <div class="instr-block__number">2</div>
              </div>
            </div>
            <div class="instr-block instr-block--last">
              <div class="instr-block__img">
                <img src="../assets/img/hand3.png" alt="how to use bot" class="instr-block__pic" />
              </div>
              <div class="instr-block__desc">
                <div class="instr-block__text">Прокачуєш знання</div>
                <div class="instr-block__number">3</div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>

    <TheFooter />
  </div>
</template>

<script>
import MainNav from "../components/MainNav";
import TheFooter from "../components/TheFooter";
import SocialLinks from "../components/SocailLinks";
import Test from "../components/Test";

export default {
  name: "Home",
  components: { MainNav, TheFooter, SocialLinks, Test }
};
</script>
