 <template>
  <div class="wrapper">
    <div class="container">
      <NavBar />
      <div class="content">
        <HeaderDescription />
        <HeaderImage />
      </div>
    </div>
    <div class="effects">
      <div class="efect-1"><fa icon="circle-notch" /></div>
      <div class="efect-2"><fa icon="plus" /></div>
      <div class="efect-3"><fa icon="plus" /></div>
    </div>
  </div>
</template>
 <script>
export default {};
</script>
<style lang="scss" scoped>
.wrapper {
  padding-bottom: 220px;
  background: var(--maincolor);
  border-radius: 0 0 200px 0;
  position: relative;
  .content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 60px;
  }
  .effects {
    .efect-1 {
      width: 30px;
      height: 25px;
      position: absolute;
      bottom: 33%;
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
      top: 16%;
      left: 18%;
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
      svg {
        width: 100%;
        height: 100%;
      }
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
@media (max-width: 537px) {
  .wrapper {
    border-radius: 0 0 0 0;
    .effects {
      .efect-1 {
        bottom: 53%;
      }
    }
  }
}
</style>