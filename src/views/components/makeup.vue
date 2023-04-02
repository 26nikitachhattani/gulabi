<template>
  <div id="app">
    <carousel
      class="mt-8"
      :autoplay="true"
      :items="3"
      style="margin: 0px 6%"
      :nav="true"
      navposition="sides"
      :responsive="{
        0: {
          items: 1,
        },
        768: {
          items: 2,
        },
      }"
    >
      <div class="mx-1">
        <v-card class="mx-3 text-center" height="400">
          <div class="text-center" align="center">
            <v-card-title class="text-center mx-10">Gulabi</v-card-title>
          </div>
          <v-img
            src="https://i.pinimg.com/originals/db/27/4f/db274fd162c3254bfa46dfe0b82f77e0.jpg"
            alt="image"
            class="ma-10"
            height="200"
          ></v-img>
        </v-card>
      </div>

      <div class="mx-1">
        <v-card class="mx-3 text-center" height="400" justify-center>
          <div class="text-center" align="center" justify-center>
            <v-card-title class="text-center" style="font-size: 30px"
              >Gulabi dekho</v-card-title
            >
          </div>
          <v-img
            src="https://mir-s3-cdn-cf.behance.net/project_modules/max_1200/ed5a3179024277.5cbca8251c762.gif"
            alt="image"
            class="ma-10"
            height="200"
          ></v-img>
        </v-card>
      </div>
      <div class="mx-1">
        <v-card class="mx-3 text-center" height="400">
          <div class="text-center mx-auto" align="center">
            <v-card-title class="text-center mx-10">Gulabi</v-card-title>
          </div>
          <v-img
            src="https://school.mangoanimate.com/wp-content/uploads/2020/07/Top-2D-Animation-Software-4-770x513.jpg"
            alt="image"
            class="ma-10"
            height="200"
          ></v-img>
        </v-card>
      </div>
      <div class="mx-1">
        <v-card class="mx-3 text-center" height="400" justify-center>
          <div class="text-center" align="center" justify-center>
            <v-card-title class="text-center mx-auto" style="font-size: 30px"
              >Gulabi dekho</v-card-title
            >
          </div>
          
          <v-img
            src="https://mir-s3-cdn-cf.behance.net/project_modules/max_1200/f1812379024277.5cbcada09cedf.gif"
            alt="image"
            class="ma-10"
            height="200"
          ></v-img>
        </v-card>
      </div>
    </carousel>
  </div>
</template>
<script src="/node_modules/jquery/dist/jquery.js"></script>
<script src="/node_modules/owl.carousel/dist/owl.carousel.min.js"></script>
<script>
//import carousel from "v-owl-carousel";
import carousel from "vue-owl-carousel";
import Vue from "vue";
Vue.use(carousel);
export default {
  name: "offersbanners",

  components: {
    carousel,
  },
  data: () => ({
    login: false,
    token: localStorage.getItem("token"),
  }),
  mounted() {},
  methods: {
  },
};
</script>
<style scoped>
.owl-theme .owl-nav [class*="owl-"] {
  color: #fff;
  font-size: 14px;
  margin: 5px;
  padding: 4px 7px;
  background: #d6d6d6;
  display: inline-block;
  cursor: pointer;
  display: none;
  border-radius: 3px;
}
.owl-carousel .owl-nav .owl-prev,
.owl-carousel .owl-nav .owl-next {
  font-weight: bold;
  font-size: 50px;
  font-family: monospace;
  padding: 10px 20px;
  display: none;
  background: #fff;
}
img {
  height: 200px;
  width: 400px;
  margin: 10px;
}
div.owl-next {
  background: #fff;
}
.owl-theme .owl-nav [class*="owl-"] {
  color: #fff;
  font-size: 14px;
  margin: 5px;
  padding: 4px 7px;
  background: #fff;
  cursor: pointer;
  display: none !important;
  border-radius: 3px;
}
.owl-theme > .owl-dots > .owl-dot:active > span,
.owl-theme .owl-dots .owl-dot:hover span {
  background: #484498 !important;
}
</style>
<style>
.owl-next {
  background: #fff !important;
}
.owl-prev {
  background: #fff !important;
}
</style>
