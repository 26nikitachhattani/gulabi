<template>
  <div id="app" class="shadedfill" style="padding: 30px 0">
    <carousel
      class=""
      :autoplay="true"
      :items="3"
      style="margin: 0px 2%"
      :nav="true"
      navposition="sides"
      :responsive="{
        0: {
          items: 1,
        },
        768: {
          items: 3,
        },
      }"
    >
      <div class="mx-1">
        <v-card class="px-auto text-center" height="300">
          <v-img
            src="https://i.pinimg.com/originals/db/27/4f/db274fd162c3254bfa46dfe0b82f77e0.jpg"
            alt="image"
            class=""
            height="200"
          ></v-img>
        </v-card>
      </div>

      <div class="mx-1">
        <v-card class="mx-3 text-center" height="300" justify-center>
          <v-img
            src="https://mir-s3-cdn-cf.behance.net/project_modules/max_1200/ed5a3179024277.5cbca8251c762.gif"
            alt="image"
            class=""
            height="200"
          ></v-img>
        </v-card>
      </div>
      <div class="mx-1">
        <v-card class="mx-3 text-center" height="300">
          <v-img
            src="https://school.mangoanimate.com/wp-content/uploads/2020/07/Top-2D-Animation-Software-4-770x513.jpg"
            alt="image"
            class="mx-10"
            height="200"
          ></v-img>
        </v-card>
      </div>
      <div class="mx-1">
        <v-card class="mx-3 text-center" height="300" justify-center>
          <v-img
            src="https://mir-s3-cdn-cf.behance.net/project_modules/max_1200/f1812379024277.5cbcada09cedf.gif"
            alt="image"
            class="mx-10"
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
    // ...mapActions("snackbar", ["showSnack"]),
    // logincheck() {
    //   alert(this.token);
    //   if (this.token != null) {
    //     alert(token);
    //     this.getoffers();
    //   }
    // },
    // getoffers() {
    //   // if (this.token != null) {
    //   const SuccessHandler = (res) => {
    //     console.log(res.data);
    //     this.banners = res.data;
    //   };
    //   const ErrorHandler = (res) => {
    //     console.log(res.data);
    //     this.showSnack({
    //       text: res.data,
    //       color: "error",
    //       timeout: 4500,
    //     });
    //   };
    //   baseaxios.request_GET(
    //     "api/banner/home-banner/",
    //     {},
    //     {},
    //     SuccessHandler,
    //     ErrorHandler,
    //     false,
    //     false
    //   );
    // },
  },
};
</script>
<style scoped>
.shadedfill {
  background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
  background-size: 400% 400%;
  animation: gradient 9s ease infinite;
  /* height: 100vh; */
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
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
