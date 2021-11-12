<template>
    <div class="slick-wrapper">
                  <!-- <div v-for="card in cards" :key="card.id" class="card">
              <fa icon="hamburger" />
              <h1>{{ card.name }}</h1>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                Nostrum, voluptas voluptates aliquid culpa inventore repudiandae
                quibusdam consectetur necessitatibus qui, error sunt sit modi
                aliquam?.
              </p>
            </div> -->
          <div
            v-swiper="swiperOption"
            class="w-5/6 ml-auto relative"
            :loadtheme="false"
          >
            <div class="swiper-wrapper">
              <div class="swiper-slide" v-for="carousel in cards" :key="carousel.id">
                <!-- Render original HTML in server, render Swiper in browser (client) -->
                <h1>{{carousel.name}}</h1>
              </div>
            </div>
            <div class="swiper-button-prev" slot="button-prev"></div>
            <div class="swiper-button-next" slot="button-next"></div>
          </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      cards: [
        { id: 1, name: "Home" },
        { id: 2, name: "Features" },
        { id: 3, name: "Screenshots" },
        { id: 4, name: "Testimonials" },
        { id: 5, name: "Pricing" },
        { id: 6, name: "Contact" },
      ],
    };
  },
};
</script>