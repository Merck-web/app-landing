<template>
  <div class="slick-wrapper">
    <div class="owl-items">
      <no-ssr>
        <carousel
          :loop="true"
          :autoplay="false"
          :responsive="{
            0: { items: 1, nav: false, center: true, margin: 10 },
            800: { items: 2, nav: false, center: true, margin: 0 },
            1264: { items: 3, nav: false },
          }"
        >
          <div v-for="card in cards" :key="card.id" class="card">
            <fa :icon="card.iconName" />

            <h1>{{ card.name }}</h1>
            <p>{{ card.description }}</p>
            <div class="efect-car">
              <div class="efect-1"></div>
              <div class="efect-2"></div>
            </div>
          </div>
        </carousel>
      </no-ssr>
    </div>
  </div>
</template>
  </div>
</template>
<script>
export default {
  data() {
    return {
      cards: [
        {
          id: 1,
          iconName: "skiing",
          name: "Clean",
          description:
            "              Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio nesciunt vel eius suscipit maiores nam est quo accusantium cupiditate delectus voluptatem eos ",
        },
        {
          id: 2,
          iconName: "fan",
          name: "Auto",
          description:
            "              Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio nesciunt vel eius suscipit maiores nam est quo accusantium cupiditate delectus voluptatem eos ",
        },
        {
          id: 3,
          iconName: "shipping-fast",
          name: "Pixel",
          description:
            "              Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio nesciunt vel eius suscipit maiores nam est quo accusantium cupiditate delectus voluptatem eos ",
        },
        {
          id: 4,
          iconName: "tshirt",
          name: "Ops",
          description:
            "              Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio nesciunt vel eius suscipit maiores nam est quo accusantium cupiditate delectus voluptatem eos ",
        },
        {
          id: 5,
          iconName: "tachometer-alt",
          name: "Kek",
          description:
            "              Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio nesciunt vel eius suscipit maiores nam est quo accusantium cupiditate delectus voluptatem eos ",
        },
        {
          id: 6,
          iconName: "fighter-jet",
          name: "Vue",
          description:
            "              Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio nesciunt vel eius suscipit maiores nam est quo accusantium cupiditate delectus voluptatem eos ",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.slick-wrapper {
  width: 100%;
  height: 100%;
  h1 {
    color: var(--title-text);
  }
  p {
    color: var(--black-400);
    line-height: 25px;
    margin-top: 5px;
  }
}
.card {
  margin: 15px;
  position: relative;
  width: 350px;
  padding: 30px;
  height: 300px;
  box-shadow: var(--shadow-black-300);
  text-align: center;
  cursor: pointer;
  svg {
    color: var(--maincolor);
    width: 40px;
    height: 40px;
    z-index: 10;
  }
}
.card:hover {
  .efect-car {
    .efect-1 {
      visibility: visible;
      left: 15px;
      transition: var(--transition);
    }
    .efect-2 {
      visibility: visible;
      right: 15px;
      transition: var(--transition);
    }
  }
}
.efect-car {
  .efect-1 {
    position: absolute;
    width: 30px;
    height: 30px;
    background-color: var(--color-1);
    left: -30px;
    top: 42%;
    border-radius: 50%;
    visibility: hidden;
    transition: var(--transition);
  }
  .efect-2 {
    position: absolute;
    width: 20px;
    height: 20px;
    background-color: var(--color-2);
    right: -20px;
    top: 80%;
    border-radius: 50%;
    visibility: hidden;
    transition: var(--transition);
  }
}
@media (max-width: 440px) {
  .card {
    width: 300px;
    height: 450px;
    padding-right: 50px;
    padding-left: 50px;
  }
}
</style>
