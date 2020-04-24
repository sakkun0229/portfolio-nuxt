<template>
  <v-container class="works" fluid>
    <v-card class="mx-auto mt-8 px-8 py-10" max-width="900" elevation="4">
      <v-card-title class="justify-center">
        <h2 class="display-2 font-weight-light mb-8">Works</h2>
      </v-card-title>

      <v-layout wrap>
        <v-flex xs12 sm6 md4 pa-2 v-for="item in items" :key="item.url">
          <v-card height="100%" elevation="4">
            <v-card-subtitle>
              <a :href="item.url" target="_blank" rel="noopener">
                <v-img :src="item.img"></v-img>
              </a>
            </v-card-subtitle>
            <v-card-text>
              <p>{{ item.text }}</p>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-card>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      title: 'Works'
    }
  },
  data() {
    return {
      items: [
        {
          url: 'https://nuxt-todo-app.netlify.app/',
          img: require('@/assets/nuxt-todo-app.png'),
          text: 'Nuxt学習用に作ったTODOアプリ。Vuexのストア経由でFirebaseと通信させています。'
        },
        {
          url: 'https://sakuma-takahisa.github.io/LP-practice/',
          img: require('@/assets/LPpractice.png'),
          text: 'コーディング練習ページ。フレームワークやjQueryを使用せずにスタイルや動きなども作成してみました。'
        },
        {
          url: 'https://sakuma-takahisa.github.io/portfolio/',
          img: require('@/assets/bootstrapLP.png'),
          text: 'Bootstrapの練習がてら作成したLP的なページ'
        }
      ]
    }
  }
}
</script>
