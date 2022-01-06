<template>
  <div class="wrapper-header">
    <div class="box-image">
      <div class="circle"></div>
      <img src="img/app-screenshots/1.webp" />
    </div>
  </div>
</template>
<style lang="scss" scoped>
.box-image {
  width: 400px;
  position: relative;
  display: flex;
  justify-content: center;
  margin-right: 20px;
  img {
    max-width: 250px;
    width: 100%;
    height: 500px;
    box-shadow: (--shadow-black-100);
    animation: bounseTo_01 3s ease-in-out infinite;
  }
}
.circle {
  position: absolute;
  border: 1px solid #f7f7f7;
  width: 400px;
  height: 400px;
  top: calc(50% - 200px);
  left: calc(50% - 200px);
  border-radius: 50%;
  opacity: 0.3;
  z-index: 1;
}
.circle::before {
  content: "";
  position: absolute;
  height: 60px;
  width: 60px;
  left: 30px;
  top: 30px;
  background-color: rgba(255, 255, 255, 0.4);
  border-radius: 50%;
  transform-origin: 170px 170px;
  animation: spin_01 10s linear infinite;
}
@keyframes spin_01 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes bounseTo_01 {
  0%,
  100% {
    transform: translateY(-30px);
  }
  50% {
    transform: translateY(0px);
  }
}
@media (max-width: 800px) {
  .box-image {
    margin-top: 60px;
  }
}
@media (max-width: 420px) {
  .box-image {
    margin-right: 0;
    width: 320px;
  }
  .circle {
    width: 320px;
    height: 320px;
    top: calc(50% - 160px);
    left: calc(50% - 160px);
  }
  .circle::before {
    left: 5px;
    transform-origin: 155px 130px;
  }
}
</style>