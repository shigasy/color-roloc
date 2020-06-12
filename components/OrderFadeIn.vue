<template>
  <div class="order-fade-in">
    <div class="order-fade-in__item1">要素1</div>
    <div class="order-fade-in__item2">要素2</div>
    <div class="order-fade-in__item3">要素3</div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.order-fade-in {
  @include center-flex;
  &__item1 {
    width: 100px;
    height: 200px;
    background-color: #ff6b6b;
    opacity: 0;
    // forwards: アニメーション終了後にキーフレームアニメーションで指定した要素を適用
    animation: fade-in 1s ease 1s forwards;
  }
  &__item2 {
    width: 300px;
    height: 100px;
    background-color: #228ae6;
    opacity: 0;
    animation: fade-in 1s ease 1.7s forwards;
  }
  &__item3 {
    width: 200px;
    height: 200px;
    background-color: #40c057;
    opacity: 0;
    animation: fade-in 1s ease 0.5s forwards;
  }
  @keyframes fade-in {
    0% {
      opacity: 0;
      transform: translateY(-15px);
    }
    100% {
      opacity: 1;
      transform: translateY(0);
    }
  }
}
</style>
