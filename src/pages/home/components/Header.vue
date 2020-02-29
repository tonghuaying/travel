<template>
<div class="header">
    <div class="header-left">
        <span class="iconfont back-icon">&#xe739;</span>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe63e;</span>
        输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
          <!-- <span>{{this.$store.state.city}}</span> -->
          <span>{{this.city}}</span>
          <span class="iconfont">&#xe673;</span>
      </div>
    </router-link>
</div>

</template>
<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  props: {
    // city: String
  },
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
 .header
    display: flex;
    line-height: $headerHeight
    background: $bgcolor
    color: #fff
    .header-left
      width: .64rem
      float: left
      padding-left: .08rem
      display: block
    .header-input
        flex: 1
        height: .64rem
        margin-left: .22rem
        background: #fff
        margin-top: .12rem
        border-radius: .1rem
        color: #ccc
        line-height: .64rem
        padding-left: .3rem
    .header-right
      min-width: 1.24rem
      flota: right
      text-align: center
      color: #fff
</style>
