<template>
  <div class="index">
    <div class="container">
      <div class="ave">
        <Avetures />
      </div>
    </div>
    <div class="facts-section"><Facts /></div>
    <AppScreen />
    <div class="download">
      <div
        class="background"
        :style="{ backgroundImage: `url(${backgroundUrl})` }"
      >
        <DownloadApp />
      </div>
      <div class="bg-opacity"></div>
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
.download {
  position: relative;
}
.background {
  padding: 50px 0;
  background-size: auto 200%;
  background-repeat: no-repeat;
  background-position: 46% -20px;
  align-items: center;
  position: relative;
  box-shadow: inset 0 0 0 200vw rgba($color: #7956fe, $alpha: 0.7);
}
</style>
