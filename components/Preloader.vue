<template>
  <transition name="fade">
    <div v-if="show" class="wrap-preloader">
      <div class="load_box">
        <div class="bar bar1"></div>
        <div class="bar bar2"></div>
        <div class="bar bar3"></div>
        <div class="bar bar4"></div>
        <div class="bar bar5"></div>
        <div class="bar bar6"></div>
      </div></div
  ></transition>
</template>
<script>
export default {
  data() {
    return {
      show: true,
    };
  },
  mounted() {
    this.showToogle();
  },
  methods: {
    showToogle() {
      setTimeout(() => {
        this.show = false;
      }, 2000);
    },
  },
};
</script>
<style lang="scss" scoped>
.wrap-preloader {
  background-color: #1f1f1f;
  width: 100%;
  min-height: 100vh;
}
.load_box {
  z-index: 100000;
  background-color: #1f1f1f;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  .bar {
    width: 4vh;
    height: 4vh;
    border-radius: 4vh;
    background-color: #fff;
    margin-right: 1vw;
    animation: 1.5s loading infinite ease-in-out;
    &.bar1 {
      animation-delay: 0.1s;
    }
    &.bar2 {
      animation-delay: 0.2s;
    }
    &.bar3 {
      animation-delay: 0.3s;
    }
    &.bar4 {
      animation-delay: 0.4s;
    }
    &.bar5 {
      animation-delay: 0.5s;
    }
    &.bar6 {
      animation-delay: 0.6s;
    }
  }
}
@keyframes loading {
  0% {
    background-color: #fff;
    transform: scale(0.1);
    opacity: 0.1;
  }
  50% {
    background-color: #00a7c2;
    transform: scale(1);
    opacity: 1;
  }
  100% {
    background-color: #fff;
    transform: scale(0.1);
    opacity: 0.1;
  }
}
</style>