<template>
  <div>
    <div class="container">
      <h1>可変長無限ループスライダー</h1>
    </div>
    <slider-color />
    <section class="order-fade-in-section">
      <order-fade-in />
    </section>
    <scroll-fade-in-opacity
      >透明度のみフェードイン<slider
    /></scroll-fade-in-opacity>

    <br />
    <br />
    <br />
    <scroll-fade-in>下からフェードイン<slider-color /></scroll-fade-in>
    <br />
    <br />
    <br />

    <scroll-fade-in-reaction
      >反動あり下からフェードイン <slider-color
    /></scroll-fade-in-reaction>
    <div style="height: 500px;">要素</div>
    <div style="height: 500px;">要素</div>
    {{ data }}
    <nuxt-link to="about">遷移 </nuxt-link>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      data: ''
    }
  },
  async created() {
    // これをページ表示後にやるのはボトルネックを解消できそう。スケルトンにしておいて。
    // こういうAPI通信完了後にレンダリングするメリットはそれほどないと思う
    const res = await fetch('http://www.mocky.io/v2/5ed897933100006700c4e577')
    const json = await res.json()
    this.data = json
    console.log(this.data)
    setTimeout(() => {
      console.log('a')
    }, 3000)
  },
  mounted() {
    setTimeout(() => {
      console.log('a')
    }, 3000)
  }
})
</script>

<style lang="scss" scoped>
.container {
  @include center-flex;
}
.order-fade-in-section {
  margin: 60px;
}
</style>
