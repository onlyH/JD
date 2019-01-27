<template lang="html">
  <div>
    <Heador/>
    <Slider/>
    <Novice/>
    <Footor/>
    <Navbar/>
  </div>
</template>

<script>
  import Heador from "../public/header.vue";
  import Navbar from "../public/navbar.vue";
  import Footor from '../public/footer.vue';
  import Slider from "./hslider.vue";
  import Novice from "./novice.vue"

  export default {
    components: {
      Heador, Footor, Navbar, Slider, Novice
    }
  };
</script>

