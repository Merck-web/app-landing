<template>
  <div class="app-screen-wrap-carousel">
    <div class="owl-items">
      <no-ssr>
        <carousel
          :loop="true"
          :autoplay="false"
          :responsive="{
            0: { items: 1, nav: false, center: true, margin: 0 },
            650: { items: 2, nav: false, center: true, margin: 0 },
            800: { items: 3, nav: false, center: true, margin: 0 },
            1264: { items: 4, nav: false },
          }"
        >
          <div v-for="screen in screens" :key="screen.id" class="screen">
            <img :src="screen.imgId" />
          </div>
        </carousel>
      </no-ssr>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      screens: [
        {
          imgId: "img/app-screenshots/1.png",
        },
        {
          imgId: "img/app-screenshots/2.png",
        },
        {
          imgId: "img/app-screenshots/3.png",
        },
        {
          imgId: "img/app-screenshots/3.png",
        },
        {
          imgId: "img/app-screenshots/2.png",
        },
        {
          imgId: "img/app-screenshots/1.png",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.app-screen-wrap-carousel{
    padding: 0 15px;
}
.screen {
  width: 250px;
  max-height: 525px;
  cursor: pointer;
}
@media (max-width: 650px) {
  .screen {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .owl-carousel .owl-stage-outer{
      width: 320px !important;
  }
}
</style>