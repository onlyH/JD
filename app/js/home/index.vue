<template lang="html">
  <div>
    <Heador/>
    <Slider/>
    <Novice/>
    <Borrow/>
    <Money/>
    <Product/>
    <Left/>
    <Footor/>
    <Navbar/>
  </div>
</template>

<script>
  import Heador from "../public/header.vue"
  import Navbar from "../public/navbar.vue"
  import Novice from "./novice.vue"
  import Borrow from "./borrow.vue"
  import Money from "./money.vue"
  import Product from './product.vue'
  import Left from "./life.vue"
  import Footor from '../public/footer.vue'
  import Slider from "./hslider.vue"

  export default {
    components: {
      Heador, Footor, Navbar, Slider, Novice, Borrow, Money, Product, Left
    }
  };
</script>

