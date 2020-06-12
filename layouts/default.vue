<template>
  <div>
    <!-- <transition name="fade"> -->
    <!-- <div v-if="isActive" class="loading">loading</div> -->
    <!-- </transition> -->
    <!-- <transition name="fade"> -->
    <nuxt />
    <!-- </transition> -->
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      isActive: true
    }
  },
  created() {
    setTimeout(() => {
      this.isActive = false
      console.log('open')
    }, 3000)
  }
})
</script>

<style scoped>
.trans {
  transition: all 0.5s cubic-bezier(0.55, 0, 0.1, 1);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.loading {
  width: 100vw;
  height: 100vh;
  background: #fff;
}

/* .loading-bg {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1;
  display: none;
  width: 100%;
  height: 100%;
  background: #000;

  /* animation: hideop 1s linear 0s; */

/*
@keyframes hideop {
  0% {
    opacity: 1;
  }

  100% {
    display: none;
    opacity: 0;
  }
} */

.hidden {
  display: none;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}

.is-active {
  width: 100vw;
  height: 100vh;
  background: #868e96;
  animation: fadeIn 3s, 3s 1s forwards;
}
</style>
