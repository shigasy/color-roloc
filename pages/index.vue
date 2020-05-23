<template>
  <div class="container">
    <logo />
    <p>ほげほげ</p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Logo from '@/components/Logo.vue'

export default Vue.extend({
  components: {
    Logo
  }
})
</script>

<style lang="scss" scoped>
.container {
  color: $color-accent;
}
</style>
