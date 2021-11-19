<template>
  <div class="client__carousel">
    <div class="container mr">
      <div class="owl-items">
        <no-ssr>
          <carousel
            :loop="false"
            :autoplay="false"
            :nav="false"
            :center="false"
            :responsive="{
              0: { items: 1 },
              1000: { items: 2 },
              1400: { items: 3 },
            }"
          >
            <div
              v-for="testimonial in testimonials"
              :key="testimonial.id"
              class="testimonial"
            >
              <div class="img">
                <img class="face" :src="testimonial.imgId" />
                <!-- <div class="after"><img src="img/icons/viruses-solid.svg" /></div> -->
              </div>
              <p class="com">{{ testimonial.comment }}</p>
              <p class="name">{{ testimonial.name }}</p>
              <p class="work">{{ testimonial.work }}</p>
              <div class="star_box">
                <div><img src="img/icons/star.svg" alt="otziv" /></div>
                <div><img src="img/icons/star.svg" alt="otziv" /></div>
                <div><img src="img/icons/star.svg" alt="otziv" /></div>
                <div><img src="img/icons/star.svg" alt="otziv" /></div>
                <div><img src="img/icons/star.svg" alt="otziv" /></div>
              </div>
            </div>
          </carousel>
        </no-ssr>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      testimonials: [
        {
          imgId: "img/testimonial/1.jpg",
          comment:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi nobis veritatis eaque.",
          name: "Name Client",
          work: "UI Designer",
          star: "5",
        },
        {
          imgId: "img/testimonial/2.jpg",
          comment:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi nobis veritatis eaque.",
          name: "Name Client",
          work: "UI Designer",
          star: "5",
        },
        {
          imgId: "img/testimonial/3.jpg",
          comment:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi nobis veritatis eaque.",
          name: "Name Client",
          work: "UI Designer",
          star: "5",
        },
        {
          imgId: "img/testimonial/4.jpg",
          comment:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi nobis veritatis eaque.",
          name: "Name Client",
          work: "UI Designer",
          star: "5",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.client__carousel{
  width: 100%;
  height: 100%;
}
.mr {
  margin-right: 100px;
}
.testimonial {
  margin: 15px;
  padding: 30px 40px;
  box-shadow: var(--shadow-black-300);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  max-width: 360px;
  .face {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 4px solid var(--maincolor);
    position: relative;
  }
  .img {
    padding-bottom: 40px;
  }
  .com {
    padding-bottom: 30px;
    font-size: 14px;
    color: var(--black-400);
    font-weight: 300;
  }
  .name {
    padding-bottom: 10px;
    font-weight: 600;
    font-size: 18px;
  }
  .work {
    padding-bottom: 20px;
    font-size: 14px;
    color: var(--black-400);
    font-weight: 300;
  }
  //   .after {
  //     position: absolute;
  //     width: 30px;
  //     height: 30px;
  //     background-color: var(--maincolor);
  //     border-radius: 50%;
  //     left: 26%;
  //     top: 20%;
  //     display: flex;
  //     justify-content: center;
  //     align-items: center;
  //     img {
  //       width: 20px;
  //       height: 20px;
  //       line-height: 30px;
  //       filter: invert(100%) sepia(0%) saturate(7495%) hue-rotate(339deg)
  //         brightness(99%) contrast(105%);
  //     }
  //   }
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
}
@media (max-width: 956px) {
  .testimonial {
    padding: 20px 120px;
  }
}
@media (max-width: 450px) {
  .testimonial {
    padding: 20px 0;
    width: 85vw;
    min-width: 85vw;
  }
}
</style>