<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/bd/8e4a1c3f470d3702.jpg_750x200_f1f0a8c7.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/de/df09fa61aed2d502.jpg_750x200_67472739.jpg'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/da/b3e1828f79777302.jpg_750x200_aed8bec6.jpg'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/f5/ea83238744f31102.jpg_750x200_73b8477c.jpg'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/6a/18f9b171a9275c02.jpg_750x200_97cd5547.jpg'
      }, {
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg'
      }, {
        id: '0007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/97/f282eaa627305102.jpg_750x200_bfa4f1aa.jpg'
      }, {
        id: '0008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/3c/c72a1ccd4d7b2202.jpg_750x200_b88bbab4.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
 .wrapper >>> .swiper-pagination-bullet-active
   background #fff
 .wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 26.67%
  background #eee
  .swiper-img
    width 100%
</style>
