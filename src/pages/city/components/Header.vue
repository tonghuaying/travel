<template>
    <div class="header">
        城市选择
        <router-link to="/">
            <span class="iconfont header-back">&#xe739;</span>
        </router-link>
    </div>
</template>
<script>
export default {
  name: 'CityHeader'

}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
  overflow: hidden
  height: $headerHeight
  line-height: $headerHeight
  text-align: center
  color: #fff
  background: $bgcolor
  font-size: .32rem
  position: relative
  .header-back
     position: absolute
     left: .2rem
     top: 0
     color: #fff
     font-size: .32rem
</style>
