<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-hotplace></home-hotplace>
    <home-guesslike></home-guesslike>
    <home-weeken></home-weeken>
</div>

</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
// import HomeRecommend from './components/recommend'
import HomeHotplace from './components/Hotplace'
import HomeGuesslike from './components/Guesslike'
import HomeWeeken from './components/Weeken'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotplace,
    HomeGuesslike,
    HomeWeeken
  }
}
</script>
<style scoped>

</style>
