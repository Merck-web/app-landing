<template>
  <div class="wrap-carousel">
    <div class="container mr">
      <div class="owl-items">
        <no-ssr>
          <carousel
            :loop="true"
            :autoplay="false"
            :nav="false"
            :center="false"
            :responsive="{
              0: { items: 1, margin: 10 },
              1100: { items: 2 ,margin: 10 },
              1400: { items: 3, margin: 10 },
            }"
          >
            <div v-for="team in teams" :key="team.id" class="team">
              <div class="img">
                <img class="face" :src="team.imgId" />
              </div>
              <p class="com">{{ team.comment }}</p>
              <p class="name">{{ team.name }}</p>
              <p class="work">{{ team.work }}</p>
            </div>
          </carousel>
        </no-ssr>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      teams: [
        {
          imgId: "img/team/1.jpg",
          name: "Name teammate",
          work: "UI Designer",
        },
        {
          imgId: "img/team/2.jpg",
          name: "Name teammate",
          work: "UI Designer",
        },
        {
          imgId: "img/team/3.jpg",
          name: "Name teammate",
          work: "UI Designer",
        },
        {
          imgId: "img/team/4.jpg",
          name: "Name teammate",
          work: "UI Designer",
        },
        {
          imgId: "img/team/5.jpg",
          name: "Name teammate",
          work: "UI Designer",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.wrap-carousel{
  width: 100%;
  height: 100%;
}
.owl-items {
  margin-right: 20px;
}
.team {
  padding: 30px;
  box-shadow: var(--shadow-black-100);
  margin: 15px;
  border-radius: 5px;
  .face {
    margin-bottom: 20px;
  }
  .name {
    padding-bottom: 20px;
    text-transform: capitalize;
    font-weight: 600;
  }
  .work {
    padding-bottom: 20px;
    color: var(--black-400);
    text-transform: capitalize;
  }
}
@media (max-width: 980px) {
  .team {
    width: 90vw;
    min-width: 90vw;
  }
}
</style>