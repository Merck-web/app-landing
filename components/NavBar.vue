<template class="nav">
  <div class="wrapper-nav">
    <div class="row">
      <div class="name-app">
        <p>Your App <fa @click="active" icon="hamburger" /></p>
      </div>
      <ul :class="{ active: !!activeUl }">
        <li
          :class="{ active: current === link || current === null }"
          @click="current = link"
          v-for="link in links"
          :key="link.id"
        >
          <a :href="link.anchor">{{ link.link }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>
 <script>
export default {
  data() {
    return {
      links: [
        { id: 1, link: "Home", anchor: "#home" },
        { id: 2, link: "Features", anchor: "#features" },
        { id: 3, link: "Screenshots", anchor: "#screenshots" },
        { id: 4, link: "Testimonials", anchor: "#testimonials" },
        { id: 5, link: "Pricing", anchor: "#pricing" },
        { id: 6, link: "Contact", anchor: "#contact" },
      ],
      current: 0,
      activeUl: false,
    };
  },
  methods: {
    active() {
      this.activeUl = !this.activeUl;
    },
  },
  mounted() {
    this.current = this.links[0];
    // this.handleSCroll();
  },
};
</script>
<style lang="scss" scoped>
.wrapper-nav {
  padding-top: 35px;
}
.row {
  justify-content: space-between;
  align-items: center;
  color: white;
  padding: 0 5px;
  ul {
    display: flex;
    justify-content: space-between;
    li:not(:last-child) {
      margin-right: 40px;
    }
    li {
      cursor: pointer;
      position: relative;
      transition: var(--transition);
      &.active {
        &.active:before {
          content: "";
          position: absolute;
          width: 100%;
          height: 2px;
          left: 0;
          bottom: 0;
          background-color: white;
        }
      }
    }
  }
  .name-app {
    cursor: pointer;
    line-height: 32px;
    font-size: 26px;
    font-weight: bold;
    svg {
      display: none;
    }
  }
}
@media (max-width: 800px) {
  .row {
    display: block;
    ul {
      width: 500px;
      height: 200px;
      background-color: var(--maincolor);
      box-shadow: var(--shadow-black-100);
      border-radius: 20px;
      position: fixed;
      top: 10px;
      right: calc(50% - 250px);
      flex-direction: column;
      display: flex;
      margin: 0 auto;
      text-align: center;
      z-index: 10;
      transform: translateY(-200%);
      transition: var(--transition);
      li {
        margin-right: 0 !important;
        &.active {
          &.active:before {
            max-width: 100px;
            left: 40%;
          }
        }
      }
      li:not(:last-child) {
        margin-bottom: 10px;
      }
      &.active {
        transition: var(--transition);
        transform: translateY(0);
      }
    }
    .name-app {
      p {
        display: flex;
        justify-content: space-between;
        padding: 0 10px;
      }
      svg {
        display: flex;
        z-index: 100;
      }
    }
  }
}
@media (max-width: 537px) {
  .row {
    ul {
      width: 300px;
      right: calc(50% - 150px);
      li {
        &.active {
          &.active:before {
            left: 34%;
          }
        }
      }
    }
  }
}
</style>