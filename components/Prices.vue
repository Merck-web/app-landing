<template>
  <div class="wrap-prices">
    <div v-for="price in prices" :key="price.id" class="card-price">
      <p class="name">{{ price.name }}</p>
      <p class="order">
        <span>$</span>{{ price.order }}<span class="monthly">/monthly</span>
      </p>
      <ul v-for="service in services" :key="service.id">
        <li><fa icon="check" />{{ service.serv1 }}</li>
        <li><fa icon="check" />{{ service.serv2 }}</li>
        <li><fa icon="check" />{{ service.serv3 }}</li>
        <li><fa icon="check" />{{ service.serv4 }}</li>
        <li><fa icon="check" />{{ service.serv5 }}</li>
      </ul>
      <button>{{ price.btn }}</button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      prices: [
        { name: "Basic", order: 99, btn: "get started" },
        { name: "Premium", order: 149, btn: "get started" },
        { name: "Ultimate", order: 199, btn: "get started" },
      ],
      services: [
        {
          serv1: "5Gb Bandwidth",
          serv2: "Free update",
          serv3: "high regular printing",
          serv4: "branding",
          serv5: "another great feature",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.wrap-prices {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 30px;
  width: 100%;
  padding: 0 15px;
  .card-price {
    width: 360px;
    box-shadow: var(--shadow-black-300);
    padding: 30px 0;
    align-items: center;
    text-align: center;
    .name {
      font-weight: 800;
      font-size: 20px;
      border-bottom: 1px solid var(--border-bottom);
      margin-bottom: 17px;
      padding-bottom: 17px;
        color: var(--title-text);
    }
    .order {
      display: flex;
      justify-content: center;
      font-size: 60px;
      font-weight: bold;
      color: var(--maincolor);
      padding-bottom: 50px;
      span {
        font-size: 14px;
        color: var(--black-400);
        font-weight: normal;
      }
      .monthly {
        display: flex;
        align-items: flex-end;
      }
    }
    ul {
      padding: 0 40px;
      text-align: left;
      li {
        font-size: 14px;
        line-height: 12px;
        color: var(--black-400);
        margin-bottom: 35px;
        text-transform: capitalize;
        padding-bottom: 5px;
        border-bottom: 1px solid var(--border-bottom);
      }
      li:last-child {
        margin-bottom: 45px;
      }
      svg {
        margin-right: 10px;
        color: var(--maincolor);
      }
    }
    button {
      background-color: var(--maincolor);
      padding: 20px 30px;
      border-radius: 50px;
      text-transform: capitalize;
      color: white;
      box-shadow: var(--shadow-black-100);
      cursor: pointer;
    }
  }
}
@media (max-width: 1280px) {
  .wrap-prices {
    grid-template-columns: repeat(2, 1fr);
    .card-price {
      align-self: center;
      justify-self: center;
    }
  }
}
@media (max-width: 770px) {
  .wrap-prices {
    grid-template-columns: repeat(1, 1fr);
  }
}
@media (max-width: 380px) {
  .wrap-prices {
    .card-price {
      width: 280px;
    }
  }
}
</style>