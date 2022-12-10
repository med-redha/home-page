<template>
  <div class="home">
    <div class="app_bar">
      <v-app-bar :elevation="0" rounded>
        <div class="app_barCntnt">
          <div class="logo"></div>
          <v-spacer></v-spacer>
          <div class="btn-tabs">
            <v-btn></v-btn>
            <v-btn></v-btn>
            <v-btn></v-btn>
            <v-btn></v-btn>
            <v-btn></v-btn>
          </div>
        </div>
      </v-app-bar>
    </div>
    <div class="sections_Container">
      <v-row>
        <v-col cols="8">
          <div class="section_one">
            <div class="hero_section">
              <img class="hero_img" src="" alt="" />
            </div>
            <div class="cntnt_holder">
              <div class="left_cntnt"></div>
              <div class="right_cntnt">
                <div></div>
                <v-btn></v-btn>
              </div>
            </div>
          </div>
        </v-col>
        <v-col cols="4">
          <div class="section_two">
            <div class="st_head">new</div>
            <div class="st_cntnt">
              <div class="st_cntntTitle"></div>
              <div class="st_cntntSubtitle"></div>
            </div>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <div class="section_three"></div>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomePage",
  props: {},
};
</script>
