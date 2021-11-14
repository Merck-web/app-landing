<template>
  <div class="wrapper-ave">
    <div class="container">
      <div class="title">
        <div class="row">
          <h1>Awesome <span>Features</span></h1>
        </div>
      </div>
      <div class="carousel">
          <SlickAventures />
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
.title {
  padding: 90px 0 90px;
  .row {
    justify-content: center;
    span {
      color: var(--maincolor);
    }
  }
}
.carousel {
  .row {
    width: 100%;
    height: 100%;
  }
}
@media (max-width: 440px) {
.title {
  .row {
    h1 {
      display: block;
      text-align: center;

    }
    span {
      display: block;
      text-align: center;
    }
  }
}
}
</style>