<template>
    <div class="weeken">
      <div class="weeken-title">周末去哪儿</div>
      <ul class="weeken-list">
        <li class="weeken-list-item" v-for="item of list" :key="item.id">
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
