<template>
<div>
    <div class="search">
       <input v-model="keyword" class="search-input" type="text" placeholder="输入城市名或拼音" />
    </div>
    <!-- <div class="search-content">
      <ul>
        <li class="search-item" v-for="item of list" :key="item.id">{{item.name}}</li>
      </ul>
    </div> -->
</div>
</template>
<script>
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  }

}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.search
  height: .72rem
  padding: 0 .1rem
  background: $bgcolor
  .search-input
     width: 100%
     height: .62rem
     line-height: .62rem
     text-align: center
     border-radius: .06rem
     color: #666
     box-sizing: border-box
     padding: 0 .1rem
.search-content
   position: absolute
   top: 1.58rem
   left: 0
   right: 0
   bottom: 0
   overflow: hidden
   z-index: 1
   background: #eee
   .search-item
      line-height: .62rem
      padding-left: .2rem
      color: #666
      border-bottom: solid 1px #ddd
</style>
