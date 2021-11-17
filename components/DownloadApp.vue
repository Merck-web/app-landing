<template>
  <div class="container">
    <div class="app">
      <div class="row jcc">
        <h1>Download <span>app</span></h1>
      </div>

      <div class="row jcc">
        <div class="cardAppBox">
          <AppCards />
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.app {
  text-align: center;
  .jcc {
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 1;
  }
  h1 {
    padding: 40px 0 20px;
    z-index: 1;
    color: white;
    text-transform: capitalize;
  }
  span {
    color: var(--maincolor);
    z-index: 1;
  }
}
</style>