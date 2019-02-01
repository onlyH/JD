<template>
  <Panel title="" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item"></div>
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
  @import "../../css/element";

  .panel {
    @include panel;
    .content {
      .item {

      }
    }
  }
</style>