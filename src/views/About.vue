<template>
<div>
  <div class="about d-flex">
  <!-- <v-card
    class="mx-auto my-2 py-0 rounded hidden-sm-and-down"
    height="400"
    width=""
    elevation="0"
  >
  <img src="https://t4.ftcdn.net/jpg/01/30/40/05/360_F_130400578_ydtJTigsl4Z5p6QihkfnsVDzDEO9eClS.jpg" alt="Ratonero" class="rounded-xl h-36 w-full object-cover">
  </v-card> -->
      <v-container >
        <v-row class="justify-center">

          <v-col cols="12" md="3" sm="6" xs="6" class="text-center justify-center" align="center" v-for="todo in 12" :key="todo">
            <v-card height="250" class="product ">
              <v-img src="https://t4.ftcdn.net/jpg/01/30/40/05/360_F_130400578_ydtJTigsl4Z5p6QihkfnsVDzDEO9eClS.jpg" class="" height="150"/>
              <v-card-text class="d-flex">
                <div class="text-left">
                  <h4>Product</h4>
                </div>
                <v-spacer></v-spacer>
                <div class="text-right">
                  <v-icon color="red">mdi-heart-outline</v-icon>
                </div>
              </v-card-text>
            </v-card>
            
          </v-col>
        </v-row>
      </v-container>
  </div>
</div>
</template>
<script>
export default {
  data () {
      return {
        items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Account', icon: 'mdi-account-box' },
          { title: 'Admin', icon: 'mdi-gavel' },
          { title: 'Admin', icon: 'mdi-gavel' },
          { title: 'Admin', icon: 'mdi-gavel' },
          { title: 'Admin', icon: 'mdi-gavel' },
        ],
      }
    },
}
</script>
<style scoped>
.product {
  /* background: linear-gradient(to right, #7387e5, #89ff86); */
 /* background: linear-gradient(180deg, #7200cc 0%, #2a7ebc 100%); */
}
</style>