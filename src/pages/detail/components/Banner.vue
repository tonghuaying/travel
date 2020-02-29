<template>
<div>
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" :src="bannerImg" />
        <div class="banner-info">
            <div class="banner-number">
                <span class="iconfont like-icon">&#xe635;</span> {{this.bannerImgs.length}}
            </div>
            <div class="banner-title">{{this.sightName}}</div>
        </div>
    </div>
    <fade-animation>
      <common-gallary :imgs="bannerImgs" v-show="showGallary" @close="handleCloseGallary"></common-gallary>
    </fade-animation>
</div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    bannerImgs: Array
  },
  data () {
    return {
      showGallary: false
    }
  },
  components: {
    CommonGallary,
    FadeAnimation
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
