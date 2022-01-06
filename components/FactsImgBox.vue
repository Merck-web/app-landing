<template>
  <div class="imgBox-wrap">
    <img src="img/app-screenshots/2.webp" />
  </div>
</template>
<style lang="scss" scoped>
.imgBox-wrap {
  width: 100%;
  img {
    width: 244px;
    height: 525px;
  }
}
@media (max-width: 900px) {
  .imgBox-wrap {
    display: flex;
    justify-content: center;
    img {
      width: auto;
      padding-bottom: 20px;
    }
  }
}
</style>