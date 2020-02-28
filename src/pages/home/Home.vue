<template>
<div>
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconsList"></home-icons>
    <home-hotplace :list="placeList"></home-hotplace>
    <home-guesslike :list="likeList"></home-guesslike>
    <home-weeken :list="weekenList"></home-weeken>
</div>

</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHotplace from './components/Hotplace'
import HomeGuesslike from './components/Guesslike'
import HomeWeeken from './components/Weeken'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotplace,
    HomeGuesslike,
    HomeWeeken
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconsList: [],
      placeList: [],
      likeList: [],
      weekenList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('api/index.json').then(this.getHomeInfoSucc).catch((e) => {
        console.log('error')
      })
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret) {
        const data = res.data
        this.city = data.city
        this.swiperList = data.swiperList
        this.iconsList = data.iconsList
        this.placeList = data.placeList
        this.likeList = data.likeList
        this.weekenList = data.weekenList
      }
      // console.log(res)
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>
<style scoped>

</style>
