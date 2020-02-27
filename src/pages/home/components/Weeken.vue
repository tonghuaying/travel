<template>
    <div class="weeken">
      <div class="weeken-title">周末去哪儿</div>
      <ul class="weeken-list">
        <li class="weeken-list-item" v-for="item of weekenList" :key="item.id">
          <div class="weeken-img">
            <img class="weeken-img-content" :src="item.url" />
          </div>
          <p class="weeken-name">{{item.name}}</p>
          <p class="weeken-desc">{{item.desc}}</p>
        </li>
      </ul>
    </div>
</template>
<script>
export default {
  name: 'HomeWeeken',
  data () {
    return {
      weekenList: [
        {
          id: '0001',
          url: 'static/images/weeken1.jpg',
          name: '深圳周边游',
          desc: '远离城市拥堵，去周边开启清新假期吧。'
        },
        {
          id: '0002',
          url: 'static/images/weeken2.jpg',
          name: '清远周边逛',
          desc: '人人都有一双发现美的眼睛，身边的事物最熟悉不过，那你可曾发现了被人遗漏的美？'
        },
        {
          id: '0003',
          url: 'static/images/weeken3.jpg',
          name: '浮在海上的绿洲',
          desc: '南国滨海之城，避寒胜地，有暖暖的阳光，海风习习，吃着海鲜逛逛老街多惬意啊'
        },
        {
          id: '0004',
          url: 'static/images/weeken4.jpg',
          name: '深圳必打卡',
          desc: '来到深圳，你需要来这里签到'
        },
        {
          id: '0005',
          url: 'static/images/weeken5.jpg',
          name: '粤东泡汤好去处',
          desc: '全时四季的温泉，度假的天堂，这里独特的矿物质温泉是您养生、养颜疗神的宝地'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';
.weeken
   background: #fff
   .weeken-title
      background: #eee
      padding-left: .2rem
      height: .9rem
      line-height: .9rem
      font-size: .3rem
   .weeken-list
      margin-bottom: .4rem
      .weeken-list-item
          margin-bottom: .4rem
          .weeken-img
              height: 2.84
              width: 100%
              .weeken-img-content
                 width: 100%
          .weeken-name
              padding-left: .2rem
              font-size: .28rem
              line-height: .7rem
              color: #333
          .weeken-desc
              padding-left: .2rem
              font-size: .24rem
              color: #999
              width: 100%
              ellipsis()

</style>
