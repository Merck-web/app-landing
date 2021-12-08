<template>
  <div class="wrap-theme">
    <div @click="toogleTheme" class="icon-box">
      <fa v-if="sun" class="sun" icon="sun" />
      <fa v-if="moon" class="moon" icon="moon" />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      sun: true,
      moon: false,
      theme: "",
    };
  },
  methods: {
    toogleTheme() {
      this.sun = !this.sun;
      this.moon = !this.moon;
      if (this.moon === true) {
        document.body.classList.add("dark");
      } else {
        document.body.classList.remove("dark");
      }
      this.save();
    },
    save() {
      window.localStorage.setItem("sun", this.sun);
      window.localStorage.setItem("moon", this.moon);
    },
  },
  mounted() {
    const body = document.querySelector("body");
    window.addEventListener("unload", () => {
      localStorage.setItem("sun", body.classList.contains("dark") ? 0 : 1);
      localStorage.setItem("moon", body.classList.contains("dark") ? 1 : 0);
    });
    if (localStorage.getItem("sun") == 1) {
      document.body.classList.remove("dark");
      this.sun = true;
      this.moon = false;
    } else if (localStorage.getItem("moon") == 1) {
      document.body.classList.add("dark");
      this.sun = false;
      this.moon = true;
    }
  },
};
</script>
<style lang="scss" scoped>
.wrap-theme {
  .icon-box {
    svg {
      padding: 7px;
      width: 100%;
      height: 100%;
    }
    .sun {
      filter: invert(81%) sepia(42%) saturate(6286%) hue-rotate(8deg)
        brightness(101%) contrast(112%);
    }
    .moon {
      filter: invert(100%) sepia(0%) saturate(0%) hue-rotate(93deg)
        brightness(103%) contrast(103%);
    }
  }
}
</style>