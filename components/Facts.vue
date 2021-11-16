<template>
  <div class="container ">
    <div class="row facts">
      <div class="imgBox"><FactsImgBox /></div>
      <div class="factsBox"><FactsBox /></div>
    </div>
  </div>
</template>
<style lang="scss" scoped>

.facts {
  padding: 50px 0 50px 90px;
  min-height: 100vh;
  align-items: center;
}
.imgBox {
  flex: 0 0 35%;
  max-width: 30%;
  padding: 0 15px;
}
.factsBox {
  flex: 0 0 65%;
  max-width: 70%;
  padding-left: 155px;
}
@media (max-width: 1264px) {
  .factsBox {
    padding-left: 30px;
  }
}
@media (max-width: 900px) {
  .imgBox,
  .factsBox {
      flex: 0 0 100%;
      max-width: 100%;
      padding-left: 0;
      padding-right: 0;
  }
  .facts{
      padding-right: 90px;
  }
}
@media (max-width: 450px) {
  .facts{
      padding-right: 20px;
      padding-left: 20px;
  }
}
</style>