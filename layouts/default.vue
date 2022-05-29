<template>
  <v-app dark>
    <v-app-bar
      absolute
      app
      color="white"
    >
      <v-toolbar-title>
        <nuxt-link to="">
          <h1>
            <v-img src="/images/Colore_toprogo.jpg" />
          </h1>
        </nuxt-link>

      </v-toolbar-title>
      <v-spacer />
      <v-btn text>キーワードから作る配色</v-btn>
      <v-btn text>心理的配色</v-btn>
      <v-btn text>店舗・商品のメージ配色</v-btn>
    </v-app-bar>
    <v-main>
      <v-container class="pa-0" fluid>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer>
      <v-container>
        <v-row>
          <v-col align="center">
            <v-btn text>キーワードから作る配色</v-btn>
            <v-btn text>心理的配色</v-btn>
            <v-btn text>店舗・商品のイメージ配色</v-btn>
            <v-btn text>運営者情報</v-btn>
            <v-btn text>問い合わせ</v-btn>
          </v-col>
        </v-row>
      </v-container>
      <v-container>
        <v-row>
          <v-col align="center">
            <span>&copy; {{ new Date().getFullYear() }}</span>
          </v-col>
        </v-row>
      </v-container>

    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
    }
  },
}
</script>
