<template>
  <Panel title="导航条" :class="$style.panel">
    <ul :class="$style.content">
      <li v-for="info in infos">
        <router-link :to="{ name: info.href}">
          <img :src=info.url>
          <p>{{info.title}}</p>
        </router-link>
      </li>
    </ul>
  </Panel>
</template>
<script>
  import Panel from "../core/panel.vue";

  export default {
    components: {Panel},
    data() {
      return {
        infos: [
          {
            href: 'home',
            url: "//img12.360buyimg.com/jrpmobile/jfs/t1/931/18/14488/935/5bda58fdE542c2cc7/f29a349a4ed750ca.png?width=60&height=60",
            title: "首页"
          },
          {
            href: 'money',
            url: "//img12.360buyimg.com/jrpmobile/jfs/t1/93/2/15333/2159/5bda590eE721487cd/85ef52d2b68205ef.png?width=60&height=60",
            title: "赚钱"
          },
          {
            href: 'borrow',
            url: "//img12.360buyimg.com/jrpmobile/jfs/t1/9698/36/4230/594/5bda5919Ec55e200a/dd949177311f04e7.png?width=60&height=60",
            title: "借钱"
          },
          {
            href: 'save',
            url: "//img12.360buyimg.com/jrpmobile/jfs/t1/4948/14/14022/816/5bda5924Eb28b0d4c/fde0775f7c0e197d.png?width=60&height=60",
            title: "省钱"
          },
          {
            href: 'vip',
            url: "//img12.360buyimg.com/jrpmobile/jfs/t1/5465/19/13992/926/5bda5932Ed6569f64/e58f749c755abad7.png?width=60&height=60",
            title: "金融会员"
          },
        ]
      }
    }
  }
</script>
<style lang='scss' module>
  @import "../../css/element";

  .panel {
    @include panel;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    height: 100px;
    margin: 0;
    > h4 {
      display: none;
    }
    .content {
      @include flex(row);
      justify-content: space-around;
      li {
        text-align: center;
        a {
          text-decoration: none;
        }
        img {
          width: 44px;
          height: 44px;
          display: inline-block;
          margin: 12px auto 6px;
        }
        p {
          font-size: 22px;
          color: #656565;
        }
      }
    }
  }
</style>
