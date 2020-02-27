<template>
    <div class="guess-like">
        <div class="guess-title">
            <span class="iconfont like-icon">&#xe635;</span>
            猜你喜欢
        </div>
        <div class="guess-like-list">
            <ul class="guess-like-ul">
                <li class="guess-like-li" v-for="item of likeList" :key="item.id">
                    <div class="guess-like-img">
                        <img class="like-img-content" :src="item.url" />
                    </div>
                    <div class="guess-like-content">
                        <p class="content-title">{{item.title}}</p>
                        <div class="star-box">
                            <span class="iconfont star-icon">&#xe6a6;</span>
                            <span class="iconfont star-icon">&#xe6a6;</span>
                            <span class="iconfont star-icon">&#xe6a6;</span>
                            <span class="iconfont star-icon">&#xe6a6;</span>
                            <span class="comment">{{item.comment}}条评论</span>
                        </div>
                        <p class="like-price"><span class="num">¥{{item.price}}</span>起</p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
  name: 'HomeGuesslike',
  data () {
    return {
      likeList: [
        {
          id: '0001',
          url: 'static/images/place1.jpg',
          title: '梦幻百花洲',
          comment: '5578',
          price: 25
        },
        {
          id: '0002',
          url: 'static/images/place2.jpg',
          title: '观音山旅游风景区',
          comment: '5578',
          price: 25
        },
        {
          id: '0003',
          url: 'static/images/place3.jpg',
          title: '水濂山乐民游艺园',
          comment: '56',
          price: 25
        },
        {
          id: '0004',
          url: 'static/images/place4.jpg',
          title: '乐民冰雪世界',
          comment: '578',
          price: 25
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
.guess-title
    height: .94rem
    line-height: .94rem
    padding-left: .2rem
    background: #fff
    .like-icon
      color: red
.guess-like-list
    .guess-like-li
       display: flex
       .guess-like-img
         width: 2rem
         height 2rem
         margin: .2rem
         .like-img-content
           width: 100%
       .guess-like-content
          width: calc(100% - 2.5rem)
          margin-top: .2rem
          padding-top: .2rem
          .content-title
            font-size: .32rem
            margin-bottom: .1rem
          .star-box
            color: orange
            margin-bottom: .4rem
            .star-icon
               font-size: .2rem
            .comment
               color: #999
          .like-price
               font-size: .24rem
               .num
                   font-size: .36rem
                   color: #ff8300

</style>
