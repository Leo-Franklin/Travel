<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide>
        <img class="swiper-img" src="@/assets/images/swiper_one.png" />
      </swiper-slide>
      <swiper-slide>
        <img class="swiper-img" src="@/assets/images/swiper_two.png" />
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
      }/* ,
      swiperList: [{
        id: '0001',
        imgUrl: '@/assets/images/swiper_one.png'
      }, {
        id: '0002',
        imgUrl: '@/assets/images/swiper_two.png'
      }] */
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow:hidden
    width: 100%
    height: 0
    padding-bottom: 26%
    background: #eee
    .swiper-img
      width: 100%
</style>
