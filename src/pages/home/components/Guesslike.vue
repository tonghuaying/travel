<template>
    <div class="guess-like">
        <div class="guess-title">
            <span class="iconfont like-icon">&#xe635;</span>
            猜你喜欢
        </div>
        <div class="guess-like-list">
            <ul class="guess-like-ul">
                <router-link tag="li" class="guess-like-li" v-for="item of list" :key="item.id" :to="'/detail/' + item.id" >
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
                </router-link>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
  name: 'HomeGuesslike',
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
