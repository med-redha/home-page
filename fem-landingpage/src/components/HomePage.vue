<template>
  <div class="home">
    
    <div class="sections_Container ">
      <v-row>
        <v-col md="8" sm="12"  cols="12">
          <div class="section_one">
            <div class="hero_section">
              <picture>
  <source media="(min-width: 900px)" srcset="../assets/images/image-web-3-desktop.jpg">
  <source media="(max-width: 899px)" srcset="../assets/images/image-web-3-mobile.jpg">
  <img  class="hero_img"  src="../assets/images/image-web-3-desktop.jpg" alt="">
  
</picture>
            </div>
            <div class="cntnt_holder">
              <div class="left_cntnt">
                <p class="left_txt">The Bright Future of Web 3.0?</p>
              </div>
              <div class="right_cntnt">
                <p class="right_txt">
                  We dive into the next evolution of the web that claims to put
                  <br />
                  the power of the platforms back into the hands of the people.
                  But is it really fulfilling its promise
                </p>
                <v-hover v-slot="{hover}">
                <v-btn class="hello_btn" :class="hover ? 'hbtn_hover' : ''">Read More</v-btn>
              </v-hover>
              </div>
            </div>
          </div>
        </v-col>
        <v-col  md="4" sm="12" cols="12">
          <div class="section_two">
            <div class="st_head">New</div>
            <div
              class="st_cntnt"
              v-for="(item, index) in sectionTwo"
              :key="index"
            >
            <v-hover v-slot="{hover}">
              <div class="st_cntntTitle" :class="hover ? 'secTwo_titleHover' : ''">{{ item.title }}</div>
            </v-hover>
              <div class="st_cntntSubtitle">{{ item.subtitle }}</div>
              <div class="devider"></div>
            </div>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col   cols="12">
          <div class="section_three  ">
            <component-one
              v-for="(dig, index) in components"
              :key="index"
              :dig="dig"
            />
          </div>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
import retro from "../assets/images/image-retro-pcs.jpg";
import keys from "../assets/images/image-top-laptops.jpg";
import ps4 from "../assets/images/image-gaming-growth.jpg";
import componentOne from "./componentOne.vue";
export default {
  components: { componentOne },
  name: "HomePage",
  data() {
    return {
      components: [
        {
          img: retro,
          head: "01",
          title: "Reviving Retro PCs",
          subtitle: "What happens when old PCs are given modern upgrades",
        },
        {
          img: keys,
          head: "02",
          title: "Top 10 Laptops Of 2022",
          subtitle: "Our best picks for various needs and budgets",
        },
        {
          img: ps4,
          head: "03",
          title: "The growth of gaming ",
          subtitle: "How the pandemic has sparked fresh oprotunities",
        },
      ],
      sectionTwo: [
        {
          title: "Hydrogen VS Electric Cars",
          subtitle: "Will hydrogen-fuled cars ever catch up to EVs?",
        },

        {
          title: "The Downsides of AI Artistry",
          subtitle:
            "What are the possible adverse effects of on-demand AI image generation?",
        },

        {
          title: "Is VC Funding Drying Up",
          subtitle:
            "Private funding by VC firms is down 50% YOY. We take a look at what that means. ",
        },
      ],
    };
  },
};
</script>
