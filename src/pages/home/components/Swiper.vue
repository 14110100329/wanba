<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
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
        imgUrl: '//pic4.40017.cn/index/slide/2017/03/21/11/86PQJh.jpg'
      }, {
        id: '0002',
        imgUrl: '//pic4.40017.cn/index/slide/2017/02/11/21/Upv1S6.jpg'
      }, {
        id: '0003',
        imgUrl: '//pic4.40017.cn/index/slide/2017/03/21/14/jLvNMj.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #eee
  .wrapper
    overflow:hidden
    width: 100%
    hight: 0
    background: #eee
    .swiper-img
      width: 100%
</style>
