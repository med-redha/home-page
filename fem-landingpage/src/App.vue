<template>
  <v-app>
    <v-container>
      <v-app-bar app color="white" class="bar" flat >
        <div class="d-flex align-center">
          <v-img
            alt=""
            class="shrink mr-2"
            contain
            src="./assets/images/logo.svg"
            transition="scale-transition"
            width="65"
          />
        </div>

        <v-spacer></v-spacer>

        <div class="btn_holder">
          <v-btn text class="bar_btn">
            <span class="mr-2">Home</span>
          </v-btn>
          <v-btn text>
            <span class="mr-2">New</span>
          </v-btn>
          <v-btn text>
            <span class="mr-2">Trending</span>
          </v-btn>
          <v-btn text>
            <span class="mr-2">Categories</span>
          </v-btn>
        </div>
      </v-app-bar>

      <v-main>
        <home-page />
      </v-main>
    </v-container>
  </v-app>
</template>

<script>
import HomePage from "./components/HomePage.vue";

export default {
  name: "App",

  components: {
    HomePage,
  },

  data() {
    return {};
  },
};
</script>
<style lang="scss">
@import "./style/main.scss";
</style>
