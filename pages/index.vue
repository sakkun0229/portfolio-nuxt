<template>
  <v-container class="home" fluid>
    <div class="home__wrapper text-center">
      <h1 class="display-3 font-weight-light mb-4">Takahisa Sakuma's Portfolio</h1>
      <p class="subtitle-1 "><s> vue cli&vuetifyの学習を兼ねて作成したポートフォリオサイトです。 </s></p>
      <p class="subtitle-1 ">Nuxt & Netlifyで再構築してみたよ (2020.April)</p>
    </div>
  </v-container>
</template>

<script>
export default {
  // data() {
  //   return {
  //     title: 'Hello, Nuxt!'
  //   }
  // },
  head() {
    return {
      title: "Takahisa Sakuma's Portfolio",
      meta: [{ hid: 'description', name: 'description', content: 'description' }]
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
</style>
