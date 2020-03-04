<template>
  <div>
  <div class="banner" @click="handleBannerClick">
    <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1611/8f/8f97e3c764a5acb2a3.water.jpg_600x330_e6ee7216.jpg" alt="">
    <div class="banner-info">
      <div class="banner-title">徐州乐园糖果世界</div>
      <div class="banner-number">
        <span  class="iconfont banner-icon">&#xe730;</span>39
      </div>
    </div>
  </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleBannerGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1611/32/32641f017955b14ca3.water.jpg_r_800x800_eca5f171.jpg',
        'http://img1.qunarzz.com/sight/p0/1611/e2/e2607ddc9cbe60afa3.water.jpg_r_800x800_156ff1c8.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleBannerGallaryClose () {
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
    position: relative;
    overflow :hidden
    height : 0
    padding-bottom : 55%
    .banner-img
      width :100%
  .banner-info
    display : flex;
    overflow : hidden
    position: absolute
    left:0
    right :0
    bottom : 0
    line-height :.6rem
    color:#fff
    background-image : linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
    .banner-title
        font-size :.32rem
        flex:1
        padding:0 .2rem
    .banner-number
        margin-top: .14rem;
        padding:0 .4rem
        height :.32rem
        line-height :.32rem
        border-radius :.2rem
        backgoround:rgba(0,0,0,.8)
        font-size : .24rem
        .banner-icon
          font-size :.24rem

</style>
