<template>
  <div>
    <div class="banner" @click="handleBannerClick">
     <img class="banner-img" src="//img1.qunarzz.com/sight/p0/201212/24/71e528a9f56c673393835fbb.png_600x330_88f97760.png">
     <div class="banner-info">
       <div class="banner-title">
          苏州天颐温泉
        </div>
       <div class="banner-number">
          <span class="iconfont banner-icon">&#xe632;</span>
          39
       </div>
     </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary.vue'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201212/24/71e528a9f56c673393835fbb.png_r_800x800_6051c304.png', 'http://img1.qunarzz.com/sight/p0/1411/44/1e84c338db4e7c2f443a2d15ab74e021.water.jpg_r_800x800_a7bd3b6f.jpg']
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

<style lang='stylus' scoped>
  @import '~styles/variable.styl'
  .banner
    position: relative
    overflow: hidden
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
      background-image: linear-gradient(top, rgba(0, 0, 0, 0),
         rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0 , 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
