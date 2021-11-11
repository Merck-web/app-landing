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

            <div v-for="card in cards" :key="card" class="card">
              <fa icon="hamburger" />
              <h1>{{ card.name }}</h1>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                Nostrum, voluptas voluptates aliquid culpa inventore repudiandae
                quibusdam consectetur necessitatibus qui, error sunt sit modi
                aliquam?.
              </p>
            </div>

        </div>
      </div>
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
<style lang="scss" scoped>
.card {
  width: 350px;
  padding: 40px;
  box-shadow: var(--shadow-black-300);
  text-align: center;
}
</style>