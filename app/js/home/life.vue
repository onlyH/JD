<template>
  <Panel title="生活服务" :class="$style.panel">
    <div :class="$style.content">
      <div :class="$style.item" v-for="item in items">
        <router-link :to="{name:item.href}">
          <img :src="item.src" alt="">
          <p>{{item.title}}</p>
          <p>{{item.add}}</p>
        </router-link>
      </div>
    </div>
  </Panel>
</template>
<script>
  import Panel from '../core/panel'

  export default {
    components: {Panel},
    data() {
      return {
        items: [
          {
            title: "惠加油",
            src: "//img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135",
            href: "home",
          },
          {
            title: "小白信用",
            src: "//img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132",
            href: "home",
            add:"全新升级",
          },
          {
            title: "信用卡还款",
            src: "//img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135",
            href: "home",
          },
          {
            title: "卡转让",
            src: "//img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135",
            href: "home",
          },
          {
            title: "定期还款",
            src: "//img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135",
            href: "home",
          }
        ]
      }
    }
  }
</script>
<style lang="scss" module>
  @import "../../css/element.scss";

  .panel {
    @include panel;
    .content {
      @include flex(row);
      box-sizing: border-box;
      padding-bottom: 40px;
      .item {
        width: 20%;
        text-align: center;
        a{
          text-decoration: none;
        }
        img {
          width: 90px;
          height: 90px;
        }
        p {
          font-size: 26px;
          color: #666666;
          text-overflow: ellipsis;
          overflow: hidden;
          white-space: nowrap;
          margin-top: 12px;
          &:nth-child(3) {
            color: #ff001a;
          }
        }
      }
    }
  }
</style>