<template>
  <div class="grid-wrapper">
    <div class="box">
      <div v-for="card in cards" :key="card.id" class="card">
        <p>{{ card.number }}</p>
        <p>{{ card.description }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      cards: [
        {
          number: "4000",
          description: "download",
        },
        {
          number: "200",
          description: "likes",
        },
        {
          number: "500",
          description: "5 start rating",
        },
        {
          number: "150",
          description: "awards",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.box {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 20px;

  .card {
    padding: 40px 40px;
    border-radius: 10px;
    background-color: var(--color-1);
    text-align: center;
    text-transform: uppercase;
    p {
      font-weight: bold;
      color: white;
      margin: 0;
      text-align: center;
    }
  }
  .card:nth-child(1n) {
    background-color: var(--color-1);
  }
  .card:nth-child(2n) {
    background-color: var(--color-2);
  }
  .card:nth-child(3n) {
    background-color: var(--color-3);
  }
  .card:nth-child(4n) {
    background-color: cornflowerblue;
  }
}
@media (max-width: 675px) {
  .box {
      grid-template-columns: repeat(1, 1fr);
  }
}
</style>