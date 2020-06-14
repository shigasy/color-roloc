<template>
  <div>
    <div class="hidden" :class="{ fade: isVisited }">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      isVisited: false
    }
  },
  mounted() {
    // reloadした時に、スクロールせずに表示したいから関数を実行
    this.handleScroll()
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      if (!this.isVisited) {
        // ターゲット要素のCSSの境界ボックスのTOPを0として、ビューポートTOPの距離
        const top = this.$el.getBoundingClientRect().top
        // 距離がビューポートの高さ - 150 = 少し要素が中央くらいに来るように
        this.isVisited = top < window.innerHeight - 150
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.hidden {
  opacity: 0;
}
.fade {
  /* bothでアニメーションが始まる前と終了後の状態を適応 */
  animation: fade-in 1s ease 0s both;
  @keyframes fade-in {
    0% {
      opacity: 0;
      transform: translateY(60px);
    }
    100% {
      opacity: 1;
      transform: translateY(0);
    }
  }
}
</style>
