<template>
<div>
  <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key='item.id'>
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl" />
      </div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/53/4bcd11cc3a5374.jpg_r_640x214_988a4cee.jpg',
        title: '重庆必游TOP10',
        desc: '重庆,非去不可'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/5f/276ed6784d25ee.jpg_r_640x214_2193082e.jpg',
        title: '重庆优质汤泉',
        desc: '细数重庆那些最赞的温泉'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1507/8e/f41005646c1e8e.jpg_r_640x214_65f25f65.jpg',
        title: '快乐湿身,水上狂欢',
        desc: '"快乐湿身,水上狂欢"门票低至5折起'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/48/f117e9b3bf582a.jpg_r_640x214_b8145711.jpg',
        title: '重庆大美古镇',
        desc: '行走重庆最美古镇,让你瞬间穿越千年'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1506/1e/f97881dbd07520.jpg_r_640x214_f8c25916.jpg',
        title: '本地人带你耍',
        desc: '玩转小面之都,High翻天'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .1rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
</style>
