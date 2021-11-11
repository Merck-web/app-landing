<template>
  <div class="wrapper-header">
    <div class="text">
      <p>Best mobile app</p>
      <h2>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatem,
        delectus? Consectetur, temporibus? Debitis eaque atque aut assumenda
        dolor? Natus praesentium perspiciatis cumque placeat consequatur
        delectus totam porro pariatur quidem quasi.
      </h2>
    </div>
    <div class="group-btn">
      <div class="download">
        <button>download app</button>
      </div>
      <div @click="$emit('openModal1')" class="play">
        <button><fa icon="play" /></button>
      </div>
    </div>
  </div>
</template>
</template>
 <script>
export default {
  data() {
    return {
    }
  },
  methods: {
  }
};
</script>
<style lang="scss" scoped>
.wrapper-header {
  margin-right: 160px;
  margin-left: 5px;
  .text {
    padding: 0 20px;
    p {
      line-height: 34px;
      font-weight: bold;
      font-size: 34px;
      color: var(--black-000);
      margin-bottom: 40px;
    }
    h2 {
      line-height: 25px;
      font-size: 15px;
      color: var(--black-000);
      font-weight: normal;
      margin-bottom: 43px;
    }
  }
  .group-btn {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 270px;
padding-left: 20px;
    .download {
      button {
        padding: 20px 30px;
        background-color: var(--black-100);
        box-shadow: var(--shadow-black-300);
        border-radius: 50px;
        font-size: 16px;
        color: var(--maincolor);
        text-transform: capitalize;
        font-weight: 600;
        transition: var(--transition);
      }
      button:hover {
        background-color: var(--maincolor);
        color: var(--black-100);
        transition: var(--transition);
      }
    }
    .play {
      button {
        padding: 20px;
        background-color: var(--black-100);
        box-shadow: var(--shadow-black-300);
        border-radius: 50%;
        color: var(--maincolor);
        transition: var(--transition);
        animation: pulse_01 2s ease infinite;
      }
      button:hover {
        background-color: var(--maincolor);
        color: var(--black-100);
        transition: var(--transition);
        animation: none;
        box-shadow: var(--shadow-black-300);
      }
    }
  }
}
@keyframes pulse_01 {
  0% {
    transform: scale(0.94);
    box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.7);
  }
  70% {
    transform: scale(1);
    box-shadow: 0 0 0 12px rgba(255, 255, 255, 0);
  }
  100% {
    transform: scale(0.94);
    box-shadow: 0 0 0 0 rgba(255, 255, 255, 0);
  }
}
</style>