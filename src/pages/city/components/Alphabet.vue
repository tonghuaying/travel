<template>
<ul class="list">
    <li class="item" v-for="(item, key) of list" :key="key">{{key}}</li>
</ul>
</template>
<script>

export default {
  name: 'CityAlphabet',
  props: {
    list: Object
  }

}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.list
   position: fixed
   right: 0
   top: 1.58rem
   bottom: 0;
   width: .4rem
   display: flex
   flex-direction: column
   .item
      line-height: .44rem
      text-align: center
      color: $bgcolor
</style>
