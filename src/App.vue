<script>

import Header from './components/Header.vue';
import Portfolio from './components/Portfolio.vue';
import Features from './components/Features.vue';

export default {
  components: { Header, Portfolio, Features },

  data() {
    return {
      main: { logo: "logo-2.png", isFixed: false },
      fixed: { logo: "logo.png", isFixed: true }
    }
  }
}
</script>

<template>
  <Header :logo="fixed.logo" :isFixed="fixed.isFixed"></Header>
  <main>
    <Header :logo="main.logo"></Header>
    <section class="onboarding">
      <div class="welcome-text">
        <h1>Bunzo</h1>
        <p>A Powerful Jamstack Blog Solution.</p>
        <img src="/images/icon.png" alt="">
      </div>
      <a class="btn" href="http://">view demo</a>
    </section>
    <Portfolio></Portfolio>
    <Features></Features>
  </main>
  <footer class="Footer">
    <p>Make your website come to life quickly.</p>
    <a class="btn" href="http://">buy bunzo</a>
  </footer>
</template>

<style scoped lang="scss">
.onboarding {
  background: url("/images/slider-landing.jpg") center;
  height: 120vh;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 120px;
  z-index: 1;
}

.welcome-text {
  width: 80%;
  text-align: center;
  font-size: 1.8rem;
  line-height: 65px;
  color: #fff;
}

.welcome-text h1 {
  font-size: 3.1rem;
  font-weight: bolder;
}

.onboarding a {
  margin: 20px auto 0;
}

.Footer {
  padding: 60px 7%;
  color: #fff;
  background-color: #1B1B1C;
  display: flex;
  justify-content: space-between;
}

.Footer p {
  font-size: 2rem;
}

@media screen and (max-width: 991px) {

  .onboarding {
    height: 105vh;
  }

  .Footer p {
    font-size: 1.5rem;
  }
}

@media screen and (max-width: 767px) {

  .onboarding {
    height: 100vh;
    padding-top: 60px;
  }

  .welcome-text {
    font-size: 1.5rem;
    line-height: 50px;
  }

  .Footer {
    flex-direction: column;
    text-align: center;
    align-items: center;
  }

  .Footer p {
    font-size: 1.3rem;
    margin-bottom: 20px;
  }
}</style>
