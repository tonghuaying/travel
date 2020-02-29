<template>
    <div class="list" ref="wrapper">
        <div>
            <div class="area">
                <div class="title border-topbottom" >当前城市</div>
                <div class="button-list">
                    <!-- <div class="button">{{this.$store.state.city}}</div> -->
                    <div class="button">{{this.currentCity}}</div>
                </div>
            </div>
            <div class="area">
                <div class="title border-topbottom" >热门城市</div>
                <div class="button-list">
                    <div class="button" v-for="item of hot" :key="item.id" @click="handleCityClick(item.name)">{{item.name}}</div>
                </div>
            </div>
            <div class="area" v-for="(item, key) of list" :key="key" :ref="key">
                <div class="title border-topbottom">{{key}}</div>
                <ul class="area-list">
                    <li class="area-list-item" v-for="innerItem of item" :key="innerItem.id" @click="handleCityClick(innerItem.name)">{{innerItem.name}}</li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
// import BScroll from 'better-scroll'
import { mapState, mapMutations } from 'vuex'
export default {
  name: 'CityList',
  props: {
    list: Object,
    hot: Array,
    letter: String
  },
  computed: {
    ...mapState({
      currentCity: 'city'
    })
  },
  methods: {
    handleCityClick (city) {
      // this.$store.dispatch('changeCity', city)
      // this.$store.commit('changeCity', city)
      this.changeCity(city)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  },
  mounted () {
    // console.log(this.$refs.wrapper)
    // this.scroll = new BScroll(this.$refs.wrapper)
  },
  watch: {
    letter () {
    //   console.log(this.letter)
      if (this.letter) {
        const element = this.$refs[this.letter][0]
        // console.log(element)
        this.scroll.scrollToElement(element)
      }
    }
  }

}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.border-topbottom
  &:before
    border-color: #ccc
  &:after
    border-color: #ccc
.title
  line-height: .4rem
  background: #eee
  padding: .1rem .2rem
  color: #666
  font-size: .26rem
.button-list
   padding: .1rem
   display: flex
   width: 100%
   flex-wrap: wrap
   .button
       width: 25%
       margin: .1rem
       border: solid 1px #eee
       padding: .1rem
       border-radius: .03rem
       text-align: center
.area-list
    margin-bottom: .2rem
    .area-list-item
       padding: .2rem .15rem
       border-bottom: solid 1px #dcdcdc

</style>
