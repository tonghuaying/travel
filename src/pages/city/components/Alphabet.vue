<template>
<ul class="list">
    <li
    class="item"
    v-for="item of letters"
    :key="item"
    :ref="item"
    @click="handleLetterClick"
    @touchstart.prevent="handleTouchStart"
    @touchmove="handleTouchMove"
    @touchend="handleTouchEnd"
     >{{item}}</li>
</ul>
</template>
<script>

export default {
  name: 'CityAlphabet',
  props: {
    list: Object
  },
  data () {
    return {
      touchStatus: false
    }
  },
  computed: {
    letters () {
      const letters = []
      for (let i in this.list) {
        letters.push(i)
      }
      return letters
    }
  },
  methods: {
    handleLetterClick (e) {
      // console.log(e.target.innerText)
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.touchStatus) {
        const startY = this.$refs['A'][0].offsetTop
        const touchY = e.touches[0].clientY - 79
        const index = Math.floor((touchY - startY) / 20)
        // console.log(index)
        if (index >= 0 && index < this.letters.length) {
          this.$emit('change', this.letters[index])
        }
      }
    },
    handleTouchEnd () {
      this.touchStatus = false
    }
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
