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
              <div class="star">
                <Stars :count="testimonial.star" />
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
          imgId: "img/testimonial/1.webp",
          comment:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi nobis veritatis eaque.",
          name: "Name Client",
          work: "UI Designer",
          star: "5",
        },
        {
          imgId: "img/testimonial/2.webp",
          comment:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi nobis veritatis eaque.",
          name: "Name Client",
          work: "UI Designer",
          star: "4",
        },
        {
          imgId: "img/testimonial/3.webp",
          comment:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi nobis veritatis eaque.",
          name: "Name Client",
          work: "UI Designer",
          star: "5",
        },
        {
          imgId: "img/testimonial/4.webp",
          comment:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Excepturi nobis veritatis eaque.",
          name: "Name Client",
          work: "UI Designer",
          star: "4",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.client__carousel {
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
  .img {
    position: relative;
  }
  .face {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 4px solid var(--maincolor);
  }
  .img::after {
    content: "";
    position: absolute;
    width: 30px;
    height: 30px;
    background-color: var(--maincolor);
    border-radius: 50%;
    left: 85%;
    top: 25%;
    z-index: 0;
  }
  .img::before {
    content: "";
    position: absolute;
    background-image: url(../static/img/icons/viruses-solid.svg);
    background-size: 80% 80%;
    background-position: center;
    width: 30px;
    height: 30px;
    left: 85%;
    top: 25%;
    z-index: 1;
  }
  .img {
    padding-bottom: 40px;
  }
  .com {
    padding-bottom: 30px;
    font-size: 14px;
    color: var(--black-400);
    font-weight: 300;
    line-height: 25px;
    padding-left: 5px;
    padding-right: 5px;
  }
  .name {
    padding-bottom: 10px;
    font-weight: 600;
    font-size: 18px;
    color: var(--title-text);
  }
  .work {
    padding-bottom: 20px;
    font-size: 14px;
    color: var(--black-400);
    font-weight: 300;
  }
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