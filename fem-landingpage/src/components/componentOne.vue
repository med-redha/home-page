<template>
  <div class="componentOne" :dig="dig">
    <div class="cmp_imageHolde ">
      <img class="cmp_img" :src="dig.img" alt="" />
    </div>
    <div class="cpm_txtHolder">
      <div class="cpm_header">{{dig.head}}</div>
      <div class="cmp_txt">
        <v-hover v-slot="{hover}">
        <div class="cpm_title" :class="hover ? 'cmpTitle_hover' : ''">{{dig.title}}</div>
      </v-hover>
        <div class="cpm_subtitle"> {{dig.subtitle}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    dig:Object,
  },
};
</script>
