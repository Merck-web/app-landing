<template>
  <div class="appCards">
    <div v-for="card in cards" :key="card.id" class="card">
      <img :src="card.imgId" />
      <h1>{{ card.name }}</h1>
      <p>{{ card.description }}</p>
      <button>{{ card.btn }}</button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      cards: [
        {
          name: "google pay",
          description:
            "      Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic necessitatibus nisi voluptatibus dolorum itaque veritatis optio labore?",
          imgId: "img/icons/google-play-brands.svg",
          btn: "download now",
        },
        {
          name: "apple store",
          description:
            "      Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic necessitatibus nisi voluptatibus dolorum itaque veritatis optio labore?",
          imgId: "img/icons/apple-brands.svg",
          btn: "download now",
        },
        {
          name: "microsoft store",
          description:
            "      Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic necessitatibus nisi voluptatibus dolorum itaque veritatis optio labore?",
          imgId: "img/icons/windows-brands.svg",
          btn: "download now",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.appCards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 30px;
}
.card {
  z-index: 1;
  background-color:var(--black-100);
  padding: 30px 40px;
  border-radius: 10px;
    transition:var(--transition);
  h1 {
    z-index: 1;
    font-weight: 600;
    font-size: 20px;
    text-transform: capitalize;
    padding-top: 15px;
    padding-bottom: 15px;
    color: var(--title-text);
  }
  p {
    padding-bottom: 30px;
    color: var(--black-400);
  }
  img {
    width: 20px;
    height: 30px;
    filter: invert(43%) sepia(75%) saturate(4401%) hue-rotate(235deg)
      brightness(97%) contrast(106%);
  }
  button {
    background-color: var(--maincolor);
    color: white;
    text-transform: capitalize;
    border-radius: 50px;
    padding: 15px 35px;
    box-shadow: var(--shadow-black-100);
  }
}
@media (max-width: 960px) {
  .appCards {
    grid-template-columns: repeat(2, 1fr);
    padding: 0 15px;
  }
}
@media (max-width: 600px) {
  .appCards {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>