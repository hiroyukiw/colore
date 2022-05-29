<template>
  <div class="article-page">
    <v-container>
      <v-row>
        <v-col align="center">
          <v-breadcrumbs :items="items" divider="/"></v-breadcrumbs>
        </v-col>
      </v-row>
    </v-container>
    <article class="article">

      <div class="article-headline-wrapper my-10">
        <header>
          <h1 class="article-title">タイトル</h1>
        </header>
        <div class="article-subtitle">サブタイトル</div>
      </div>

      <div>
        <v-img src="/images/antique_main.jpg" height="400"/>
      </div>

      <div class="color-pallet-title  my-12">
        <div class="article-title-second">
          <h2>タイトル2</h2>
        </div>
      </div>

      <div class="color-pallet">
        <v-sheet v-for="m in 5" :key="m">
          <v-img></v-img>
          <div class="cmyk-wrapper">
            <div class="cmyk-title">CMYK</div>
            <div class="cmyk-code">0 50 0 0</div>
          </div>
          <v-divider></v-divider>
          <div class="rgb-wrapper">
            <div class="rgb-title">CMYK</div>
            <div class="rgb-code">204 102 255</div>
          </div>
          <v-divider></v-divider>
          <div class="hex-wrapper">
            <div class="hex-title">CMYK</div>
            <div class="hex-code">#cc66ff</div>
          </div>
        </v-sheet>
      </div>

    </article>


  </div>
</template>


<script>
export default {
  name: 'SlugPage',
  data() {
    return {
      items: [
        {
          text: 'Dashboard',
          disabled: false,
          href: 'breadcrumbs_dashboard',
        },
        {
          text: 'Link 1',
          disabled: false,
          href: 'breadcrumbs_link_1',
        },
        {
          text: 'Link 2',
          disabled: true,
          href: 'breadcrumbs_link_2',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.article {
  max-width: 740px;
  margin: 0 auto;
}
.article-headline-wrapper {
  header {
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
  }
  .article-subtitle {
    text-align: center;
  }
}
.article-title-second {
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
}

.color-pallet {
  display: flex;
  justify-content: space-between;
  align-items: stretch;
  gap: 20px;
}
</style>
