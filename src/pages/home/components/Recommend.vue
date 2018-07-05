<template>
<div>
  <div class="title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key='item.id'>
        <img class="item-img" :src="item.imgUrl" />
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        desc: '上海市浦东新区川沙新镇上海迪士尼度假区'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg',
        title: '武隆天坑地缝国家地质公园',
        desc: '重庆市武隆县银杏大道武隆喀斯特旅游区'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/07/6457ef01e33f69234f30949a340f2f56.jpg_200x200_e14826a1.jpg',
        title: '重庆海昌加勒比海水世界',
        desc: '重庆市南岸区崇文路35号'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201305/31/1e09178fd22121bbc8d65eac.jpg_200x200_cd998bd6.jpg',
        title: '丰都鬼城',
        desc: '重庆市丰都县名山镇名山路152号'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1709/7b/7bf5984d7e6a3c2da3.img.jpg_200x200_5fb349d9.jpg',
        title: '重庆欢乐谷',
        desc: '重庆市渝北区金渝大道29号重庆欢乐谷'
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
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        line-height .4rem
        margin-top .16rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
