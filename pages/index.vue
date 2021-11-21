<template>
  <div class="index">
    <div class="container">
      <div class="ave">
        <Avetures />
      </div>
    </div>
    <div class="facts-section"><Facts /></div>
    <div class="app"><AppScreen /></div>
    <div class="download">
      <div
        class="background"
        :style="{ backgroundImage: `url(${backgroundUrl})` }"
      >
        <DownloadApp />
      </div>
      <div class="bg-opacity"></div>
    </div>
    <div class="how__to">
      <HowItWork />
    </div>
    <div class="what__say">
      <ClientSay />
    </div>
    <div class="pricing">
      <Pricing />
    </div>
    <div class="team">
      <Team />
    </div>
    <div class="faq">
      <FAQ />
    </div>
    <div class="get">
      <GetInTouch />
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
.what__say {
  background-color: var(--black-100);
  padding: 85px 130px;
}
.team {
  background-color: var(--black-100);
  padding: 85px 130px;
}
.get {
  background-color: var(--black-100);
  padding: 85px 15px;
}
@media (max-width: 1070px) {
  .team {
    padding: 85px 0;
  }
}
@media (max-width: 1000px) {
  .what__say {
    .owl-theme .owl-nav.disabled + .owl-dots {
      margin-top: 0;
      padding-top: 60px;
      padding-bottom: 90px;
      margin-left: 40px;
      text-align: left;
    }
  }
}
@media (max-width: 929px) {

}
@media (max-width: 573px) {
  .what__say {
    padding: 0 calc(80% - 360px);
  }
  .testimonial {
    padding: 30px 5px;
  }
}
</style>
