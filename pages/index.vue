<template>
  <div>
    <section id="hero">
      <div class="row no-gutters">
        <v-img src="/images/Colore-headerimage_02.jpg" max-height="450" position="center" />
      </div>
    </section>
    <section>
      <v-container>
        <div class="headline-wrapper my-10">
          <header class="text-center">
            <h2 class="scheme-title">Color scheme list</h2>
            <div class="scheme-subtitle">配色一覧</div>
          </header>
        </div>

      </v-container>
    </section>

    <section>
      <v-container>
        <v-row>
          <v-col
            v-for="n in 12"
            :key="n"
            cols="12"
            sm="4"
          >
            <v-hover v-slot="{ hover }">
              <v-card
                flat tile to="/"
                :class="{ 'on-hover': hover }">
                <v-img
                  src="https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg"
                >
                  <v-card-title >
                    <v-chip small color="white">カテゴリー</v-chip>
                  </v-card-title>
                </v-img>
                <v-card-title>
                  <div class="list-title">
                  タイトル
                  </div>
                </v-card-title>
                <v-card-subtitle>
                  <div class="list-subtitle">
                  タイトル
                  </div>
                </v-card-subtitle>
              </v-card>
            </v-hover>


          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="my-12">
      <v-container>
        <v-row >
          <v-col align="center">
            <v-btn outlined x-large>
              配色一覧を見る
            </v-btn>
          </v-col>

        </v-row>
      </v-container>
    </section>
  </div>

</template>

<script>
export default {
  name: 'IndexPage',
}
</script>


<style lang="scss" scoped>
.headline-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 40px;
  &::before,
  &::after {
    content: '';
    flex-grow: 1;/* 余白を分け与える */
    height: 1px;
    background: #222222;
  }
  .scheme-title {
    color: #222222;
    font-size: 22px;
  }
  .scheme-subtitle {
    color: #707070;
    font-size: 16px;
  }
}


.list-title {
  position: relative;
  padding-left: 16px;
  font-size: 20px;
  &::before {
    position: absolute;
    top: 50%;
    left: -15px;
    content: '';
    width: 15px;
    height: 1px;
    background: #222222;
  }
}

.list-subtitle {
  padding-left: 16px;
}
</style>
