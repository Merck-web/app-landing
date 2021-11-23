<template>
  <div class="wrap-accordeon">
    <div id="app">
      <v-app id="inspire">
        <v-expansion-panels focusable>
          <v-expansion-panel v-for="(information, i) in informations" :key="i">
            <v-expansion-panel-header>
              <div class="header">
                {{ information.item }}
              </div>
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <div class="content">
                {{ information.desc }}
              </div>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-app>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      informations: [
        {
          item: "100% fluid responsive",
          desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua. Utenim ad minimveniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
        },
        {
          item: "clean code",
          desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua. Utenim ad minimveniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
        },
        {
          item: "flat, modern and clean design",
          desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua. Utenim ad minimveniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
        },
        {
          item: "custom font support",
          desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed doeiusmod tempor incididunt ut labore et dolore magna aliqua. Utenim ad minimveniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.wrap-accordeon {
  width: 100%;
  padding: 0 220px;
  .content {
    padding: 20px 0 0;
    color: var(--black-400);
  }
  .header {
    text-transform: capitalize;
    font-size: 18px;
    font-weight: 500;
  }
}
.v-expansion-panel--active {
  background-color: var(--maincolor) !important;
}
@media (max-width: 1263px) {
  .wrap-accordeon {
    padding: 0 110px;
  }
}
@media (max-width: 700px) {
  .wrap-accordeon {
    padding: 0 15px;
  }
}
</style>