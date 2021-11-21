<template>
  <div class="">
    <div class="star_box">
      <div v-for="i in +count" :key="i">
        <img src="img/icons/star-solid.svg" alt="otziv" />
      </div>
      <div v-for="i in 5 - +count" :key="i+'123'">
        <img src="img/icons/star.svg" alt="otziv" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  props: {
    count: {
      type:  [
          Number , String
      ],
      default: 0,
    },
  },
  mounted() {
      console.log(this.count)
  }
};
</script>
<style lang="scss" scoped>
  .star_box {
    display: flex;
    justify-content: space-between;
    filter: invert(82%) sepia(20%) saturate(5275%) hue-rotate(345deg)
      brightness(98%) contrast(108%);
    div {
      width: 17px;
      height: 17px;
      margin-right: 3px;
    }
  }
</style>