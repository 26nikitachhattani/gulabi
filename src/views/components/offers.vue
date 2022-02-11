<template>
    <div>
        <v-carousel height="00">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      reverse-transition="fade-transition"
      transition="fade-transition"
      class=""
    >
    <div class="ma-10 px-5"  dark style="font-size:60px">
        {{item.name}}
    </div>
    </v-carousel-item>
  </v-carousel>
    </div>
</template>
<script>
  export default {
    data () {
      return {
        items: [
          {name: 'nikita lorem somebkkjnknkjnn',
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
              name: 'nikita',
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
              name: 'nikita',
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
              name: 'nikita',
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },
  }
</script>
<style scoped>
.maintool {
  /* background: linear-gradient(to right, #7387e5, #89ff86); */
  background: linear-gradient(180deg, #7200cc 0%, #2a7ebc 100%);
}
</style>