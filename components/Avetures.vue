<template>
  <div class="wrapper-ave">
    <div class="container">
      <div class="title">
        <div class="row">
          <h1>Awesome <span>Features</span></h1>
        </div>
      </div>
      <div class="carousel">
        <div class="row">
          <SlickAventures />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
    };
  },
};
</script>
<style lang="scss" scoped>
.card {
  width: 350px;
  padding: 40px;
  box-shadow: var(--shadow-black-300);
  text-align: center;
}
</style>