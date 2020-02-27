<template>
<div class="wrapper">
    <swiper :options="swiperOption" >
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img
        class="swiper-img"
        :src="item.url" />
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          url: '/static/images/swiper1.jpg'
        },
        {
          id: '0002',
          url: '/static/images/swiper3.jpg'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important;
.wrapper
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 31.25%;
    background: #eee;

.swiper-img
    width: 100%;
    height: 2.34rem;
</style>
