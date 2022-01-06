 <template>
  <div class="wrapper">
    <div class="container">
      <div @scroll="stickyNav" v-if="navModalWindow" class="nav">
        <NavBar />
      </div>

      <div id="beforeHome" class="content">
        <HeaderDescription @openModal1="openModal" />
        <HeaderImage />
      </div>
    </div>
    <div class="effects">
      <div class="efect-1"><fa icon="circle-notch" /></div>
      <div class="efect-2"><fa icon="plus" /></div>
      <div class="efect-3"><fa icon="plus" /></div>
      <div class="dark">
        <div class="dark-theme"><DarkTheme /></div>
      </div>
    </div>
    <div @openModal1="openModal()" v-if="modalWindow" class="modal-window">
      <ModalHeader @openModal1="openModal" />
    </div>
  </div>
</template>
 <script>
export default {
  data() {
    return {
      modalWindow: false,
      navModalWindow: true,
    };
  },
  methods: {
    openModal() {
      this.modalWindow = !this.modalWindow;
      this.navModalWindow = !this.navModalWindow;
      if (this.modalWindow === true) {
        const html = document.querySelector("html");
        html.style.overflow = "hidden";
      } else {
        const html = document.querySelector("html");
        html.style.overflow = "auto";
      }
    },
    stickyNav() {
      if (window.pageYOffset > 200) {
        let nav = document.querySelector(".nav");
        nav.classList.add("stickyNav");
      } else {
        let nav = document.querySelector(".nav");
        nav.classList.remove("stickyNav");
      }
    },
  },
  mounted() {
    window.onload = () => {
      console.log("loaded");
      document.querySelector("body").onscroll = () => {
        this.stickyNav();
      };
    };
  },
};
</script>
<style lang="scss" scoped>
.nav {
  position: fixed;
  left: 0;
  top: 0;
  z-index: 100;
  width: 100%;
  padding: 0 30px 10px;
}
.stickyNav {
  padding-bottom: 35px;
  background-color: var(--mainpage);
  transition: var(--transition);
}
.wrapper {
  padding-bottom: 220px;
  background: var(--mainpage);
  border-radius: var(--borderMainBlock);
  position: relative;
  transition: var(--transition);
  .content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 200px;
  }
  .effects {
    .efect-1 {
      width: 30px;
      height: 25px;
      position: absolute;
      bottom: 10%;
      left: 6%;
      color: #07c9bf;
      animation: rotate_01 10s linear infinite;
      svg {
        width: 100%;
        height: 100%;
      }
    }
    .efect-2 {
      position: absolute;
      top: 50%;
      left: 80%;
      color: #f2ad13;
      width: 25px;
      height: 25px;
      svg {
        width: 100%;
        height: 100%;
      }
    }
    .efect-3 {
      position: absolute;
      top: 10%;
      right: 5%;
      width: 30px;
      height: 30px;
      color: #bdadff;
    }
    .dark {
      box-shadow: var(--outer-shadow);
    }
    .dark-theme {
      position: fixed;
      top: 20%;
      right: 1%;
      width: 40px;
      height: 40px;
      cursor: pointer;
      text-align: center;
      font-size: 20px;
      background-color: var(--maincolor);
      box-shadow: var(--shadow-black-300);
      border-radius: 50%;
      z-index: 1000;
    }
    svg {
      width: 100%;
      height: 100%;
    }
  }
}
@keyframes rotate_01 {
  0% {
    transform: rotate(0deg);
  }
  50% {
    transform: rotate(360deg);
  }
  100% {
    transform: rotate(0deg);
  }
}
@media (max-width: 800px) {
  .content {
    flex-direction: column;
  }
  .wrapper-header {
    margin-right: 0;
  }
  .wrapper {
    padding-bottom: 100px !important;
  }
}
@media (min-width: 1024px) {
  .wrapper {
    .effects {
      .efect-2 {
        left: 97%;
      }
    }
  }
}
@media (max-width: 537px) {
  .wrapper {
    border-radius: 0 0 0 0;
    .effects {
      .efect-1 {
        bottom: 4%;
      }
      .efect-2 {
        left: 90%;
      }
    }
  }
}
</style>