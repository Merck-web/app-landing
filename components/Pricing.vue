<template>
  <div class="wrap-pricing">
    <div class="container">
      <div class="row jcc">
        <p>pricing <span>plan</span></p>
      </div>
      <div class="row">
        <Prices />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
};
</script>
<style lang="scss" scoped>
.wrap-pricing {
  padding-bottom: 90px;
}
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