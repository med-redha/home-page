<template>
  <v-app>
    <v-container>
      <v-app-bar  color="white" class="bar" flat >
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

        <div class="btn_holder && hidden-sm-and-down" >
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
        <div class="nav_drawer && hidden-sm-and-up">
          <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
          <v-navigation-drawer
      v-model="drawer"
      absolute
      bottom
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
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
    return {
      drawer: false,
      group: null,
    };
    
  },
  watch: {
      group () {
        this.drawer = false
      },
    },
};
</script>
<style lang="scss">
@import "./style/main.scss";
</style>
