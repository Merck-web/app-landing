<template>
  <div class="container">
    <div class="row jcc">
      <p>how it <span>works</span></p>
    </div>
    <div class="row">
        <How />
    </div>
  </div>
</template>
<style lang="scss" scoped>
p {
  text-transform: capitalize;
  font-weight: bold;
  padding: 90px 0 70px;
  text-align: center;
  line-height: 30px;
  font-size: 30px;
}
span {
  color: var(--maincolor);
}
.jcc {
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1;
}
</style>