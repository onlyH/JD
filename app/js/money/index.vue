<template>
  <div>
    <Heador/>
    <AdTop/>
    <Slider/>
    <Ada/>
    <Navbar/>
  </div>
</template>

<script>
  import Heador from '../public/header.vue'
  import AdTop from './adTop.vue'
  import Navbar from '../public/navbar.vue'
  import Slider from './mslider.vue'
  import Ada from './ada.vue'

  export default {
    name: "index",
    components: {Heador, AdTop, Navbar, Slider, Ada}
  }
</script>

<style scoped>

</style>