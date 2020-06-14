<template>
  <div class="cmyk">
    <slot></slot>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.cmyk {
  font-family: 'Fredoka One', sans-serif;
  font-weight: bold;
  color: #000;
  text-shadow: 0.25rem -0.25rem rgba(magenta, 0.75),
    -0.25rem -0.25rem rgba(cyan, 0.75), 0 0.5rem rgba(yellow, 0.75);
}
</style>
