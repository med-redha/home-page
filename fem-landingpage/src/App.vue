<template>
  <v-app>
    <v-container>
      <v-app-bar color="white" class="bar" flat>
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

        <div class="btn_holder && hidden-sm-and-down">
          <v-hover v-slot="{ hover }">
            <v-btn plain class="bar_btn" :class="hover ? 'btn_hover' : ''">
              <span class="mr-2">Home</span>
            </v-btn>
          </v-hover>
          <v-hover v-slot="{ hover }">
            <v-btn plain class="bar_btn" :class="hover ? 'btn_hover' : ''">
              <span class="mr-2">New</span>
            </v-btn>
          </v-hover>
          <v-hover v-slot="{ hover }">
            <v-btn plain class="bar_btn" :class="hover ? 'btn_hover' : ''">
              <span class="mr-2">Trending</span>
            </v-btn>
          </v-hover>
          <v-hover v-slot="{ hover }">
            <v-btn plain class="bar_btn" :class="hover ? 'btn_hover' : ''">
              <span class="mr-2">Categories</span>
            </v-btn>
          </v-hover>
        </div>
        <div class="nav_drawer && hidden-md-and-up">
          <v-app-bar-nav-icon
            @click.stop="drawer = !drawer"
          ></v-app-bar-nav-icon>
        </div>
      </v-app-bar>
      <v-navigation-drawer v-model="drawer" temporary app right>
        <div>
          <v-btn @click.stop="drawer = !drawer" icon
            ><v-icon>mdi-close</v-icon></v-btn
          >
        </div>
        <v-list dense>
          <v-list-item v-for="item in items" :key="item.title">
            <v-list-item-content>
              <v-list-item-title class="item_title">{{
                item.title
              }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
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
      items: [
        { title: "Home" },
        { title: "New" },
        { title: "Popular" },
        { title: "trending" },
        { title: "Categories" },
      ],
    };
  },
  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>
<style lang="scss">
@import "./style/main.scss";
</style>
