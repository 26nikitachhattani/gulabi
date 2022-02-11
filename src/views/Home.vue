<template>
  <div>
    <banners />
    <offers />
    <makeup />
  </div>
</template>

<script>
// import HelloWorld from '../components/HelloWorld'
import banners from "../views/components/banners";
import makeup from "../views/components/makeup";
import offers from "../views/components/offers";

export default {
  name: "Home",

  components: {
    // HelloWorld,
    banners,
    makeup,
    offers,
  },
};
</script>
