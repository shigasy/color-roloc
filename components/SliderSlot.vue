<template>
  <div class="slider">
    <div class="slider-container">
      <ul class="slider-container__list" :style="styles">
        <slot></slot>
      </ul>
      <ul class="slider-container__list" :style="styles">
        <slot></slot>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    speed: String
  },
  computed: {
    styles() {
      return {
        '--speed': this.speed
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.slider {
  width: 800px;
  margin-right: auto;
  margin-left: auto;
  overflow: hidden;

  &-container {
    display: flex;

    &__list {
      --speed: 10s;

      display: flex;

      /* list-style-type: none; */
      animation: slider var(--speed) 0s linear infinite;
      @keyframes slider {
        0% {
          transform: translate3d(0, 0, 0);
        }
        100% {
          transform: translate3d(-100%, 0, 0);
        }
      }
    }
  }
}
</style>
