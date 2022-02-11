<template>
  <div class="about d-flex">
               <v-card
    class="mx-auto my-2 rounded-0 hidden-sm-and-down"
    height="400"
    width="256"
    elevation="0"
  >
    <v-navigation-drawer
      class="deep-purple accent-4"
      dark
      permanent
    >
      <v-list>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <template v-slot:append>
        <div class="pa-2">
          <v-btn block>
            Logout
          </v-btn>
        </div>
      </template>
    </v-navigation-drawer>
  </v-card>
    <v-card width="100%" class="mx-auto" elevation="0">
      <v-container fluid>
        <v-row class="justify-center">

          <v-col cols="12" md="4" sm="6" xs="6" class="text-center justify-center" align="center" v-for="todo in 12" :key="todo">
            <v-card height="300" width="90%" class="product">

            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
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
        ],
      }
    },
}
</script>
<style scoped>
.product {
  /* background: linear-gradient(to right, #7387e5, #89ff86); */
 background: linear-gradient(180deg, #7200cc 0%, #2a7ebc 100%);
}
</style>