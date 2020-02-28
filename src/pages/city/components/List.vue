<template>
    <div class="list" ref="wrapper">
        <div>
            <div class="area">
                <div class="title border-topbottom">当前城市</div>
                <div class="button-list">
                    <div class="button">深圳</div>
                    <div class="button">深圳</div>
                    <div class="button">深圳</div>
                    <div class="button">深圳</div>
                </div>
            </div>
            <div class="area">
                <div class="title border-topbottom">热门城市</div>
                <div class="button-list">
                    <div class="button">深圳</div>
                    <div class="button">深圳</div>
                    <div class="button">深圳</div>
                    <div class="button">深圳</div>
                </div>
            </div>
            <div class="area">
                <div class="title border-topbottom">A</div>
                <ul class="area-list">
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                    <li class="area-list-item">city</li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    console.log(this.$refs.wrapper)
    this.scroll = new BScroll(this.$refs.wrapper)
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
