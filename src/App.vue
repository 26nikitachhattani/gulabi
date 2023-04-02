<template>
  <v-app>
    <v-toolbar app class="maintool" dark elevation="0">
      <v-icon color="white" large>mdi-cookie-outline</v-icon>
      <v-spacer></v-spacer>
      <div
        class="align-center white--text"
        style="font-size: 40px; font-family: 'comforter', cursive"
      >
        Gulabi
      </div>
      <v-spacer></v-spacer>
      <v-icon color="white " class="90-rotate" large>mdi-cart-outline</v-icon>
    </v-toolbar>
    <v-toolbar flat class="mt-0" height="80" style="padding: 0px 2px; ">
      <v-tabs
        align-with-title
        elevation="0"
        slider-size="0"
        next-icon="mdi-chevron-right-circle"
        prev-icon="mdi-chevron-left-circle"
        show-arrows
        style="font-family: poppins; "
      >
      <!-- <v-tab style="background-color: #d0daff; font-size: 20px">
        Makeup
        </v-tab>
        <v-tab style="background-color: #d7d0ff; font-size: 20px">
        Accesories
        </v-tab>
        <v-tab style="background-color: #f0c8f1">
        Ethanic Wear
        </v-tab>
        <v-tab style="background-color: #f0d0d6">
        cosmetics
        </v-tab>
         <v-tab style="background-color: #ffec80">
        Makeup
        </v-tab>
        <v-tab style="background-color: #f7d8ba">
        Makeup
        </v-tab>
        <v-tab style="background-color: #ffe7c7">
        Makeup
        </v-tab>
        <v-tab style="background-color: #fef8dd">
        Makeup
        </v-tab>
        <v-tab style="background-color: #daeaf6">
          <div><v-icon class="white--text">mdi-cookie</v-icon></div>
        Makeup
        </v-tab>
        <v-tab style="background-color: #cce0aa" to="/about">
          <div><v-icon class="white--text">mdi-note</v-icon></div>
        Makeup
        </v-tab> -->
        <v-tab style="font-family: 'poppins'">
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-book-outline</v-icon>
            </v-avatar>
            <div>Makeup</div>
          </div>
        </v-tab>
        <v-tab style="font-family: 'poppins'">
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-cookie-outline</v-icon>
            </v-avatar>
            <div>Makeup</div>
          </div>
        </v-tab>
        <v-tab>
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-necklace</v-icon>
            </v-avatar>
            <div>Accesories</div>
          </div>
        </v-tab>
        <v-tab>
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-brush</v-icon>
            </v-avatar>
            <div>dress</div>
          </div>
        </v-tab>
        <v-tab>
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-leaf</v-icon>
            </v-avatar>
            <div>Nikiya</div>
          </div>
        </v-tab>
        <v-tab>
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-lipstick</v-icon>
            </v-avatar>
            <div>makeup</div>
          </div>
        </v-tab>
        <v-tab>
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-tshirt-v</v-icon>
            </v-avatar>
            <div>Cloths</div>
          </div>
        </v-tab>
         <v-tab>
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-chart-bubble</v-icon>
            </v-avatar>
            <div>Cloths</div>
          </div>
        </v-tab>
        <v-tab>
          <div>
            <v-avatar size="46px" class="maintool">
              <v-icon class="white--text">mdi-cup</v-icon>
            </v-avatar>
            <div>Cloths</div>
          </div>
        </v-tab>
        
      </v-tabs>
    </v-toolbar>
    <v-dialog width="400" v-model="login">
      <v-card elevation="0" class="pa-4 maintool">
        <div style="margin: 0 160px">Login</div>
        <v-text-field outlined dense dark v-model="username" class="mx-2" placeholder="Username"></v-text-field>
        <v-text-field outlined dense  dark v-model="username" class="mx-2" placeholder="Username"></v-text-field>
        <v-btn class="maintool px-10 mx-2" large dark width="350">login</v-btn>
      </v-card>
    </v-dialog>

    <v-main>
      <router-view />
    </v-main>
      <v-footer dark padless>
      <v-card flat tile width="100%" class="maintool white--text text-center" elevation="0">
        <v-card-text>
          <h1 class="pb-2 white--text"> You can find us at</h1>
          <a target="_blank" v-for="social in socials" v-bind:key="social" >
            <v-btn class="mx-4 white--text" icon>
              <v-icon size="24px">{{ social.icon }}</v-icon>
            </v-btn>
          </a> 
        </v-card-text>

        <v-card-text class="pt-0 text-left text-md-center">
          <v-expansion-panels accordion v-model="panel" multiple>
            <v-expansion-panel v-for="(item,i) in items" :key="i" class="maintool col-md-3 col-12 elevation-0 ">
              <h3 class="d-none d-md-block py-2">{{ item.name }}</h3>
              <v-expansion-panel-header class="d-md-none">{{ item.name }}</v-expansion-panel-header>
              <v-expansion-panel-content>
                <li v-for="tag in item.tags" :key="tag">
                  <a target="_blank" v-bind:href="tag.url" class="white--text">{{tag.urlname}} </a>
                </li>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          Copyright 2022 - {{ new Date().getFullYear() }} <a class="white--text"
            href="https://codepen.io/jettaz">AniKriya</a> | It is free for use
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    login: false,
    username: "",
    
  panel: [],
    socials: [
      { name:"facebook", icon:"mdi-facebook", url:"https://codepen.io/jettaz"},
      {name:"twitter", icon:"mdi-twitter", url:"https://codepen.io/jettaz"},
      {name:"google", icon:"mdi-google", url:"https://codepen.io/jettaz"},
      {name:"linkedin", icon:"mdi-linkedin", url:"https://codepen.io/jettaz"},
      {name:"instagram", icon:"mdi-instagram", url:"https://codepen.io/jettaz"}
      
    ],
    items: [
      {
        name: "Product",
        tags: [
          {
            urlname: "Create Websites",
            url: "https://codepen.io/jettaz"
          },
          {
            urlname: "Secure Cloud Hosting",
            url: "https://codepen.io/jettaz"
          },
          {
            urlname: "Engage Your Audience",
            url: "https://codepen.io/jettaz"
          },
          {
            urlname: "Website Support",
            url: "https://codepen.io/jettaz"
          }
        ]
      },
      { name: "Company", 
       tags: [
         { urlname: "About", url: "https://codepen.io/jettaz" },
         { urlname: "Careers", url: "https://codepen.io/jettaz"},
         { urlname: "Support", url: "https://codepen.io/jettaz"},
         { urlname: "Pricing", url: "https://codepen.io/jettaz"},
         { urlname: "FAQ", url: "https://codepen.io/jettaz"}
       ] 
      },
      { name: "Resources", 
       tags: [
         { urlname: "Blog", url: "https://codepen.io/jettaz" },
         { urlname: "eBooks", url: "https://codepen.io/jettaz" },
         { urlname: "Whitepapers", url: "https://codepen.io/jettaz" },
         { urlname: "Comparison Guide", url: "https://codepen.io/jettaz" },
         { urlname: "Website Grader", url: "https://codepen.io/jettaz" }
       ] 
      },
      { name: "Get Help", 
       tags: [
         { urlname: "Help Center", url: "https://codepen.io/jettaz" },
         { urlname: "Contact Us", url: "https://codepen.io/jettaz" },
         { urlname: "Privacy Policy", url: "https://codepen.io/jettaz" },
         { urlname: "Terms", url: "https://codepen.io/jettaz" },
         { urlname: "Login", url: "https://codepen.io/jettaz" }
       ]
      }
    ]
  }),

  beforeDestroy() {
    if (typeof window !== "undefined") {
      window.removeEventListener("resize", this.onResize, { passive: true });
    }
  },

  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  },

  methods: {
    onResize() {
      if (window.innerWidth >= 960) {
        this.panel = [...Array(4).keys()].map((k, i) => i);
      } else {
        this.panel = [];
      }
    }
  }
};
</script>
<style>
.owl-theme .owl-nav {
    display: none !important;
    margin-top: 10px;
    text-align: center;
    -webkit-tap-highlight-color: transparent;
}
</style>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Caveat&family=Gideon+Roman&family=Noto+Sans&display=swap');
@import url("https://fonts.googleapis.com/css2?family=Comforter&family=Poppins");
@import url("https://fonts.googleapis.com/css2?family=Comforter&family=Dancing+Script:wght@400;500;600;700&display=swap");
* {
  /* font-family: "Comforter"; */
  font-family: Caveat,sans-serif;
  font-weight: 500;
  /* font-family: 'poppins', cursive; */
  /* font-family: "Pacifico", cursive; */
  letter-spacing: 0px !important;
  text-transform: capitalize !important;
  /* color: linear-gradient(180deg, #7200cc 0%, #2a7ebc 100%); */
}

.maintool {
  background: linear-gradient(180deg, #7200cc 0%, #2a7ebc 100%);
  z-index: 9999;
}
@media (min-width:960px) {
    .v-expansion-panel:before {
        box-shadow: none !important;
    }
    .v-expansion-panel:not(:first-child)::after {
        border-top: none;
    }
}
.resize {
  text-align: center;
}
.resize {
  margin-top: 3rem;
  font-size: 1.25rem;
}
/*RESIZESCREEN ANIMATION*/
.right {
  animation: rightanime 1s linear infinite;
}

.left {
  animation: leftanime 1s linear infinite;
}
@keyframes rightanime {
  50% {
    transform: translateX(10px);
    opacity: 0.5;
  }
  100% {
    transform: translateX(10px);
    opacity: 0;
  }
}
@keyframes leftanime {
  50% {
    transform: translateX(-10px);
    opacity: 0.5;
  }
  100% {
    transform: translateX(-10px);
    opacity: 0;
  }
}

</style>
