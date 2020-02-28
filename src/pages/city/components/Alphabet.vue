<template>
<ul class="list">
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
    <li class="item">A</li>
</ul>
</template>
<script>

export default {
  name: 'CityAlphabet'

}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.list
   position: absolute
   right: 0
   top: 1.58rem
   bottom: 0;
   width: .4rem
   display: flex
   flex-direction: column
   justify-content: center
   .item
      line-height: .44rem
      text-align: center
      background: $bgcolor
      color: #fff
</style>
