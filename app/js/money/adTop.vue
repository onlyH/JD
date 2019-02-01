<template>
  <Panel title="img" :class="$style.panel">
    <section :class="$style.content">
      <router-link :to="{name:'home'}">
        <img
            src="//img12.360buyimg.com/jrpmobile/jfs/t28858/7/1058667857/15792/606d0f10/5c050f76Ndb650556.png?width=750&height=120"
            alt="">
      </router-link>
    </section>
  </Panel>
</template>
<script>
  import Panel from '../core/panel'

  export default {
    components: {Panel}
  }
</script>
<style lang="scss" module>
  @import "../../css/element.scss";

  .panel {
    @include panel;

    > h4 {
      display: none;
    }

    .content {
      margin-top: 100px;
      z-index: 999;
      position: fixed;
      top: 0;
      left: 0;
      right: 0;

      img {
        width: 100%;
        display: block;
        height: 100px;
      }
    }
  }
</style>