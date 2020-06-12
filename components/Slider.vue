<template>
  <div class="slider">
    <div class="slider-container">
      <ul class="slider-container__list">
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">1</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">2</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">3</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">4</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">5</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">6</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">7</p>
        </li>
      </ul>
      <ul class="slider-container__list">
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">1</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">2</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">3</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">4</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">5</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">6</p>
        </li>
        <li class="slider-container__list--item">
          <p class="slider-container__list--text">7</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {}
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
      display: flex;

      /* list-style-type: none; */
      animation: slider 10s 0s linear infinite;
      @keyframes slider {
        0% {
          transform: translate3d(0, 0, 0);
        }
        100% {
          transform: translate3d(-100%, 0, 0);
        }
      }

      &--item {
        position: relative;
        width: 180px;
        height: 110px;
        margin: 0 20px;
        background-color: #9ac4f0;
        border: 1px solid $color-border;
      }

      &--text {
        font-size: 40px;
        font-weight: bold;
        @include center;
      }
    }
  }
}
</style>
