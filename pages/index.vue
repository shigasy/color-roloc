<template>
  <div>
    <div class="container">
      <h1>可変長無限ループスライダー</h1>
    </div>
    <slider />
    <section class="order-fade-in-section">
      <order-fade-in />
    </section>
    <scroll-fade-in-opacity
      >透明度のみフェードイン<slider
    /></scroll-fade-in-opacity>

    <br />
    <br />
    <br />
    <scroll-fade-in>下からフェードイン<slider /></scroll-fade-in>
    <br />
    <br />
    <br />

    <scroll-fade-in-reaction
      >反動あり下からフェードイン <slider
    /></scroll-fade-in-reaction>
    <div style="height: 500px;">要素</div>
    <div style="height: 500px;">要素</div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.container {
  @include center-flex;
}
.order-fade-in-section {
  margin: 60px;
}
</style>
