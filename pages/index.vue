<template>
  <v-container class="home" fluid>
    <div class="home__wrapper text-center">
      <h1 class="mb-8">
        <span
          v-for="(t, index) in text"
          :key="index"
          class="title-text display-2 font-weight-light"
          :style="{ animationDelay: index * 100 + 'ms' }"
          v-text="t"
        />
      </h1>

      <p class="subtitle-1 "><s> vue cli&vuetifyの学習を兼ねて作成したポートフォリオサイトです。 </s></p>
      <p class="subtitle-1 ">Nuxt & Netlifyで再構築してみたよ (2020.April)</p>
    </div>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      title: "Takahisa Sakuma's Portfolio"
    }
  },
  data() {
    return {
      text: "Takahisa Sakuma's Portfolio"
    }
  }
}
</script>

<style lang="scss">
.home {
  background: linear-gradient(-135deg, #00bcd4, #e0f7fa);
  width: 100vw;
  height: 100vh;
  &__wrapper {
    width: 60%;
    max-width: 800px;
    margin: 0 auto;
    margin-top: 200px;
  }
}

@keyframes text-in {
  0% {
    transform: translate(0, -20px);
    opacity: 0;
  }
}

.title-text {
  display: inline-block;
  min-width: 0.2em;
  animation: text-in 0.8s cubic-bezier(0.22, 0.15, 0.25, 1.43) 0s backwards;
}

@media screen and (max-width: 1035px) {
  h1 {
    max-width: 410px;
    margin: 0 auto;
  }
}

@media screen and (max-width: 720px) {
  h1 {
    max-width: 210px;
    margin: 0 auto;
  }
  .title-text {
    min-width: 0em;
  }
}
</style>
