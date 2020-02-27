<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img
        class="banner-img"
        src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1582740406448&di=bbd9cb9999aece8c988020f836b7cae6&imgtype=0&src=http%3A%2F%2Fimages4.c-ctrip.com%2Ftarget%2Ffd%2Ftuangou%2Fg2%2FM05%2F5D%2F09%2FCghzgVSqIPCAZ1KUAAJclE8rfX8596_720_480_s.jpg"
      />
      <div class="banner-info">
        <div class="banner-tittle">
          八达岭长城(AAAAA景区)
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe674;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    >
    </common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'Detail',
  data () {
    return {
      showGallary: false,
      imgs: ['https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1582807238102&di=ea6f9bf3697a7dc6e7997ee35a6edb95&imgtype=0&src=http%3A%2F%2Fbpic.588ku.com%2Felement_origin_min_pic%2F17%2F07%2F23%2F6b75229ba2752e24a2ec873bbaaa48d6.jpg', 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1582807238102&di=ea6f9bf3697a7dc6e7997ee35a6edb95&imgtype=0&src=http%3A%2F%2Fbpic.588ku.com%2Felement_origin_min_pic%2F17%2F07%2F23%2F6b75229ba2752e24a2ec873bbaaa48d6.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-tittle
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        line-height: .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
