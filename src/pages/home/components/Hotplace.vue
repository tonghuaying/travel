<template>
    <div class="hotplace">
        <div class="hotplace-title"><span class="iconfont hot-icon">&#xe60d;</span>本周热门榜单</div>
        <div class="hotplace-content">
            <ul class="place-ul">
                <li class="place-li" v-for="item of placeList" :key="item.id">
                    <div class="place-img">
                        <img class="place-img-content" :src="item.url" />
                    </div>
                    <p class="place-desc">{{item.desc}}</p>
                    <p class="place-price">¥<span class="number">{{item.price}}</span>起</p>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
  name: 'HomeHotplace',
  data () {
    return {
      placeList: [
        {
          id: '0001',
          url: 'static/images/place1.jpg',
          desc: '乐民水上乐园',
          price: 105
        },
        {
          id: '0002',
          url: 'static/images/place2.jpg',
          desc: '健康活水世界',
          price: 27
        },
        {
          id: '0003',
          url: 'static/images/place3.jpg',
          desc: '飘雪乐园',
          price: 28
        },
        {
          id: '0004',
          url: 'static/images/place4.jpg',
          desc: '乐民冰雪世界',
          price: 20
        },
        {
          id: '0005',
          url: 'static/images/place5.jpg',
          desc: '水濂山',
          price: 105
        },
        {
          id: '0006',
          url: 'static/images/place6.jpg',
          desc: '东城榕树湾泳健会SPA水疗',
          price: 27
        },
        {
          id: '0007',
          url: 'static/images/place7.jpg',
          desc: '龙凤山庄影视渡假村',
          price: 60
        },
        {
          id: '0008',
          url: 'static/images/place8.jpg',
          desc: '观音山旅游风景区',
          price: 68
        },
        {
          id: '0009',
          url: 'static/images/place9.jpg',
          desc: '梦幻百花洲',
          price: 25
        }
      ]
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
