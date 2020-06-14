<template>
  <div class="loading4"></div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.loading4 {
  width: 60px;
  height: 60px;
  margin: 0 auto;
  border: 5px solid #333;
  border-right: 5px solid transparent;
  border-radius: 50%;
  animation: rotate 1s linear infinite;
}

@keyframes rotate {
  100% {
    transform: rotate(360deg);
  }
}
</style>
