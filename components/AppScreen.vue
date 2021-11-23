<template>
  <div class="app-screen-wrap">
    <p>App <span>Screenshots</span></p>
    <AppScreenCarousel />
  </div>
</template>
<style lang="scss" scoped>
.app-screen-wrap {
  margin: 0 auto;
  max-width: 1120px;
  width: 100%;
  align-items: center;
  padding: 50px 0;
  p {
    text-transform: capitalize;
    font-weight: bold;
    padding: 50px 0;
    text-align: center;
    line-height: 30px;
    font-size: 30px;
    color: var(--title-text);
  }
  span {
    color: var(--maincolor);
  }
}
</style>