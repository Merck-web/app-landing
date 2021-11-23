<template>
  <div class="container">
    <div class="row jcc">
      <p>what our <span>client</span> say</p>
    </div>
    <div class="row">
        <ClientCarousel />
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
p {
  text-transform: capitalize;
  font-weight: bold;
  padding: 90px 0 70px;
  text-align: center;
  line-height: 30px;
  font-size: 30px;
  color: var(--title-text);
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