<template>
  <div>
    <slider-slot speed="30s">
      <li class="item">
        <p class="text">1</p>
      </li>
      <li class="item">
        <p class="text">2</p>
      </li>
      <li class="item">
        <p class="text">3</p>
      </li>
      <li class="item">
        <p class="text">4</p>
      </li>
    </slider-slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      speed: '1s'
    }
  }
}
</script>

<style lang="scss" scoped>
.item {
  position: relative;
  width: 180px;
  height: 110px;
  margin: 0 20px;
  background-color: #9ac4f0;
  border: 1px solid $color-border;
}

.text {
  font-size: 40px;
  font-weight: bold;
  @include center;
}
</style>
