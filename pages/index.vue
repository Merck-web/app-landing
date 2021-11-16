<template>
  <div class="index">
    <div class="container">
      <div class="ave">
        <Avetures />
      </div>
    </div>
    <div class="facts-section"><Facts /></div>
    <AppScreen />
    <div
      class="background"
      :style="{ backgroundImage: `url(${backgroundUrl})` }"
    >
    <div class="bg-opacity"></div>
      <DownloadApp />
    </div>
  </div>
</template>

<script>
import backgroundUrl from "static/img/download-app-bg.jpg";
export default {
  data() {
    return { backgroundUrl };
  },
};
</script>
<style lang="scss" scoped>
.ave {
  width: 100%;
}
.facts-section {
  background-color: var(--black-100);
}
.background {
  padding: 50px 0;
  min-height: 100vh;
  align-items: center;
  position: relative;
}
.bg-opacity{
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background: var(--maincolor);
  opacity: 0.7;
  z-index: 100;
}
</style>
