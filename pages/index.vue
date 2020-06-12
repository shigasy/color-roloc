<template>
  <div>
    <logo />
    <div class="container">
      <h1>可変長無限ループスライダー</h1>
    </div>
    <slider />
    <section class="order-fade-in-section">
      <order-fade-in />
    </section>
  </div>
</template>

<script lang="ts">
// TODO: v-forで回す
import Vue from 'vue'
import Logo from '@/components/Logo.vue'
import Slider from '@/components/Slider.vue'
import OrderFadeIn from '@/components/OrderFadeIn'

export default Vue.extend({
  components: {
    Logo,
    Slider,
    OrderFadeIn
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
