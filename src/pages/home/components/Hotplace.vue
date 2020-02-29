<template>
    <div class="hotplace">
        <div class="hotplace-title"><span class="iconfont hot-icon">&#xe60d;</span>本周热门榜单</div>
        <div class="hotplace-content">
            <ul class="place-ul">
                <router-link  tag="li" class="place-li" v-for="item of list" :key="item.id" :to="'/detail/' + item.id">
                    <div class="place-img">
                        <img class="place-img-content" :src="item.url" />
                    </div>
                    <p class="place-desc">{{item.desc}}</p>
                    <p class="place-price">¥<span class="number">{{item.price}}</span>起</p>
                </router-link>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
  name: 'HomeHotplace',
  props: {
    list: Array
  },
  data () {
    return {

    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';
.hotplace
  background: #eee
  margin-top: .1rem
  padding-top: .2rem
  padding-bottom: .2rem
  .hotplace-title
    height: .94rem
    line-height: .94rem
    padding-left: .2rem
    background: #fff
    .hot-icon
      color: orange
      display: inline-block
      margin-right: .1rem
  .hotplace-content
    width: 100%
    .place-ul
      overflow-x: auto
      height: 3rem
      display: flex
      padding: .2rem
      background: #fff
      .place-li
        display: inline-block
        margin-right: .2rem
        .place-img
          width: 2rem
          height: 2rem
          .place-img-content
            width: 100%
        .place-desc
          width: 2rem
          line-height: .5rem
          text-align: center
          ellipsis()
        .place-price
          text-align: center
          .number
            color: #ff8300
</style>
