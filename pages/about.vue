<template>
  <v-container class="about" fluid>
    <v-card class="mx-auto mt-8 px-8 py-10 text-center" max-width="750" elevation="4">
      <v-card-title class="justify-center">
        <h2 class="display-2 font-weight-light mb-10">About</h2>
      </v-card-title>

      <v-avatar color="cyan" size="180" class="mb-5">
        <v-img :src="require('@/assets/me.png')"></v-img>
      </v-avatar>
      <v-card-text>
        <h3 class="mb-6 headline text--primary">佐久間 貴久</h3>
        <p>1992年茨城出身。東京理科大学工学部第二部電気工学科卒。</p>
        <p>
          大学卒業後は音楽やりながらサービス業や音楽教室の仕事をしたりして過ごしてきました。現在はキャリアチェンジの為、Web系の言語を学習しつつ求職中です。
        </p>
        <p>昨年一年ほどスタートアップの会社でRailsの開発業務(アルバイトでしたが)の経験があります。</p>
        <p>はやくスキル身につけて食えるようになりたい()</p>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      title: 'About'
    }
  }
}
</script>
