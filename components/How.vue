<template>
  <div class="how-wrapper">
    <div class="steps">
      <div v-for="step in steps" :key="step.id" class="card">
        <div class="number">
          <p>{{ step.number }}</p>
        </div>
        <div class="hover">
          <div class="name">
            <p>{{ step.name }}</p>
          </div>
          <div class="desc">
            <p>
              {{ step.description }}
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
      steps: [
        {
          number: "1",
          name: "download",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed, iure, ducimus asperiores deleniti, minus quo vero libero natus quas facere sequi similique fugit.",
        },
        {
          number: "2",
          name: "create profile",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed, iure, ducimus asperiores deleniti, minus quo vero libero natus quas facere sequi similique fugit.",
        },
        {
          number: "3",
          name: "search product",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed, iure, ducimus asperiores deleniti, minus quo vero libero natus quas facere sequi similique fugit.",
        },
        {
          number: "4",
          name: "order",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed, iure, ducimus asperiores deleniti, minus quo vero libero natus quas facere sequi similique fugit.",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.steps {
  display: flex;
  justify-content: space-between;
  position: relative;
  padding: 0 15px;
  .card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    text-align: center;
    margin-right: 120px;
    z-index: 1;
  }
  .card:last-child {
    margin-right: 0;
  }
  .number {
    width: 60px;
    height: 60px;
    font-size: 30px;
    line-height: 60px;
    background-color: var(--maincolor);
    border-radius: 50%;
    color: #fff;
    margin-bottom: 40px;
    box-shadow: var(--shadow-black-100);
    transition: var(--transition);
  }
  .name {
    text-transform: capitalize;
    font-weight: 600;
    font-size: 20px;
    margin-bottom: 30px;
    cursor: pointer;
    color: var(--title-text);
  }
  .desc {
    padding-bottom: 140px;
    cursor: pointer;
    color: var(--black-400);
  }
}
.card:hover {
  .number {
    background-color: var(--color-1);
    transition: var(--transition);
  }
}

.steps::before {
  content: "";
  position: absolute;
  width: calc(100% - 220px);
  height: 2px;
  left: 110px;
  top: 30px;
  background-color: var(--maincolor);
  z-index: 0;
}
@media (max-width: 1264px) {
  .steps {
    .card {
      margin-right: 10px;
    }
    .card:last-child {
      margin-right: 0;
    }
  }
  .steps::before {
    left: 110px;
    width: calc(100% - 220px);
  }
}
@media (max-width: 600px) {
  .steps {
    flex-direction: column;
    justify-content: flex-start;
    padding-bottom: 140px;
    .card {
      align-items: flex-start;
      margin-bottom: 30px;
      margin-right: 0;
    }
    .card:last-child {
      margin-bottom: 0;
    }
    .desc {
      padding-bottom: 0 !important;
    }
    .name,
    .desc {
      width: 100%;
      display: flex;
      justify-content: flex-start;
      text-align: left;
      padding-left: 100px;
      margin-top: 10px;
    }
    .number {
      margin-bottom: -55px;
    }
  }
  .steps::before {
    left: 45px;
    width: 2px;
    height: calc(100% - 320px);
  }
}
@media (max-width: 400px) {
  .steps::before {
    height: calc(100% - 390px);
  }
}
@media (max-width: 280px) {
  .steps::before {
    height: calc(100% - 500px);
  }
}
</style>