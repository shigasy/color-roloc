<template>
  <div>
    <logo />
    <div class="container">
      <h1>可変長無限ループスライダー</h1>
    </div>
    <slider />
  </div>
</template>

<script lang="ts">
// TODO: v-forで回す
import Vue from 'vue'
import Logo from '@/components/Logo.vue'
import Slider from '@/components/Slider.vue'

export default Vue.extend({
  components: {
    Logo,
    Slider
  }
})
</script>

<style lang="scss" scoped>
.container {
  @include center-flex;
}
</style>
