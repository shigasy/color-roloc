<template>
  <div>
    <div class="loading" :class="{ 'loading-is-show': isLoadingTime }">
      <div class="loading-wrap">
        <cmyk
          ><h1><span class="loading-text">web</span></h1></cmyk
        >
      </div>
    </div>
    <nuxt v-if="!isLoadingTime" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      isLoadingTime: true
    }
  },
  created() {
    setTimeout(() => {
      this.isLoadingTime = false
    }, 3000)
  }
})
</script>

<style lang="scss" scoped>
.loading {
  position: fixed;
  width: 100vw;
  height: 100vh;

  // opacityのみだとjsで反応出来てしまうから
  // https://medium.com/eureka-engineering/html-css-%E3%81%9F%E3%81%8B%E3%81%8C%E3%83%95%E3%82%A7%E3%83%BC%E3%83%89%E3%82%A4%E3%83%B3-%E3%83%95%E3%82%A7%E3%83%BC%E3%83%89%E3%82%A2%E3%82%A6%E3%83%88%E3%81%99%E3%82%8B%E3%81%A0%E3%81%91%E3%81%AE%E6%8C%99%E5%8B%95%E3%81%AB%E5%85%A8%E5%8A%9B%E3%81%A7%E5%8F%96%E3%82%8A%E7%B5%84%E3%82%93%E3%81%A0%E7%B5%90%E6%9E%9C-%E6%9C%80%E5%BC%B7%E3%81%AEcss%E3%81%8C%E3%81%A7%E3%81%8D%E3%81%A6%E3%81%97%E3%81%BE%E3%81%A3%E3%81%9F%E8%A9%B1-%E6%9C%80%E5%BC%B7-881152c4ff13#result
  visibility: hidden;
  background: $color-white;
  opacity: 0;

  // 時間で制御するのはJavaScriptの方だからanimationではない
  transition: opacity 0.6s, visibility 0.6s;
  @include z-index(loading);

  /* animation: all fade-out 1s ease 3s both;
  @keyframes fade-out {
    0% {
      opacity: 1;
    }
    100% {
      opacity: 0;
    }
  } */
  &-is-show {
    visibility: visible;
    opacity: 1;
  }
  &-wrap {
    @include center;
  }
  &-text {
    font-size: 120px;
  }
}
</style>
