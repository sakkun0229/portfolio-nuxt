<template>
  <v-container class="skill" fluid>
    <v-card class="mx-auto mt-8 px-8 py-10" max-width="900">
      <v-card-title class="justify-center">
        <h2 class="display-2 font-weight-light mb-8">Skill</h2>
      </v-card-title>

      <v-layout wrap class="mb-8">
        <v-flex xs12 sm6 md4 pa-2 v-for="item in items" :key="item.title">
          <v-card height="100%" elevation="4">
            <v-card-title class="justify-center">
              <h3>{{ item.title }}</h3>
            </v-card-title>
            <v-card-text>
              <p>{{ item.text }}</p>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
      <v-flex text-center>
        <p>フロントエンド周辺(Typescript, Nuxt)やPHP(WP, Laravel)等を学習して使えるようにしていきたいです。</p>
        <p>Svelteてどうなんだろ🤔</p>
      </v-flex>
    </v-card>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      title: 'Skill'
    }
  },
  data() {
    return {
      items: [
        {
          title: 'HTML, CSS',
          text:
            '基本的なことは大体いけると思います。フレームワークはBootstarp4が使えます。SASS(SCSS)でコーディングしています。'
        },
        {
          title: 'JavaScript',
          text:
            '基本的なことはいｋ(ry。 後述のRailsと組み合わせてjQuery扱ったり、PWA化の対応なんかもかじったことがあります。'
        },
        {
          title: 'Ruby',
          text:
            '以前勤めていたアルバイトでRailsをメインに使用していました。PGとして機能実装や修正等のタスクをしていました。'
        },
        {
          title: 'Vue.js',
          text:
            'Rails + Vueの組み合わせで使用していました。こちらはそこまで経験積めなかったので今後ガシガシ勉強していきたいと思ってます。'
        },
        { title: 'Git', text: 'Githubを利用してます。ブランチ切ってPR出したりなどの基本操作が可能です。' },
        { title: 'PHP', text: '勉強中です＞＜　DockerでLAMP環境作ってLaravelあたり学習したい' },
        {
          title: 'English',
          text: '日常会話がギリギリ困るレベル。数年前にフロリダ一人旅してなんとか帰ってこれた経験があります。'
        }
      ]
    }
  }
}
</script>
