<template>
  <div class="wrap-team">
    <div class="container">
      <div class="row jcc">
        <p>team <span>member</span></p>
      </div>
      <div class="row">
        <TeamCarousel />
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
.wrap-team {
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