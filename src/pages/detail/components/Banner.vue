<template>
<div>
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" src="static/images/banner1.jpg" />
        <div class="banner-info">
            <div class="banner-number">
                <span class="iconfont like-icon">&#xe635;</span> 56
            </div>
            <div class="banner-title">八达岭长城(AAAAA景区)</div>
        </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleCloseGallary"></common-gallary>
</div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['static/images/banner1.jpg', 'static/images/banner2.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleCloseGallary () {
      this.showGallary = false
    }
  }
}
</script>
<style lang="stylus" scoped>
.banner
   overflow: hidden
   position: relative
   height: 0
   padding-bottom: 55%
   .banner-img
      width: 100%
   .banner-info
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      .banner-number
         margin-bottom: 0.08rem
         padding-left: .2rem
      .banner-title
         margin-bottom: .2rem
         padding-left: .3rem
         font-size: .38rem
</style>
