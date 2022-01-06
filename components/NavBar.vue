<template class="nav">
  <div ref="msg_wrapper" class="wrapper-nav">
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
        {
          id: 2,
          link: "Features",
          anchor: "#beforeFeatures",
          offSetTop: "beforeFeatures",
        },
        {
          id: 3,
          link: "Screenshots",
          anchor: "#beforeScreenshots",
          offSetTop: "beforeScreenshots",
        },
        {
          id: 4,
          link: "Testimonials",
          anchor: "#beforeTestimonials",
          offSetTop: "beforeTestimonials",
        },
        {
          id: 5,
          link: "Pricing",
          anchor: "#beforePricing",
          offSetTop: "beforePricing",
        },
        {
          id: 6,
          link: "Contact",
          anchor: "#beforeContact",
          offSetTop: "beforeContact",
        },
      ],
      current: 0,
      activeUl: false,
      windowTop: 0,
    };
  },
  methods: {
    active() {
      this.activeUl = !this.activeUl;
    },
    onScroll(e) {
      this.windowTop = e.target.documentElement.scrollTop;
      // console.log({ top: this.windowTop });
    },
    handlerActiveClass() {
      const screenHeight = window.screen.height;
      var home = document.getElementById("beforeHome").getBoundingClientRect();
      var features = document.getElementById("beforeFeatures").getBoundingClientRect();
      var screenshots =
        document.getElementById("beforeScreenshots").getBoundingClientRect();
      var testimonials =
        document.getElementById("beforeTestimonials").getBoundingClientRect();;
      var pricing = document.getElementById("beforePricing").getBoundingClientRect();
      var contact = document.getElementById("beforeContact").getBoundingClientRect();
      // console.log( screenHeight)
      //       console.log( home.y, features.y)
      if (screenHeight > home.y && screenHeight/2 < features.y) {
        this.current = this.links[0];
      } else if (screenHeight > features.y && screenHeight < screenshots.y) {
        this.current = this.links[1];
      } else if (screenHeight > screenshots.y && screenHeight < testimonials.y) {
        this.current = this.links[2];
      } else if (screenHeight > testimonials.y && screenHeight <  pricing.y) {
        this.current = this.links[3];
      } else if (screenHeight > pricing.y && screenHeight <  contact.y) {
        this.current = this.links[4];
      } else if (screenHeight > contact.y) {
        this.current = this.links[5];
      }
    },
  },
  mounted() {
    this.current = this.links[0];
    window.addEventListener("scroll", this.onScroll);
    window.addEventListener("scroll", this.handlerActiveClass);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
    window.removeEventListener("scroll", this.handlerActiveClass);
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