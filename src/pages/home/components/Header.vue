<template>
<div class="header">
    <div class="header-left">
        <span class="iconfont back-icon">&#xe739;</span>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe63e;</span>
        输入城市/景点/游玩主题
    </div>
    <div class="header-right">
        城市
        <span class="iconfont">&#xe673;</span>
    </div>
</div>

</template>
<script>
export default {
  name: 'Header'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
 .header
    display: flex;
    line-height: .86rem;
    background: $bgcolor;
    color: #fff;
    .header-left
      width: .64rem;
      float: left;
      padding-left: .08rem;
      display: block;
    .header-input
        flex: 1;
        height: .64rem;
        margin-left: .22rem;
        background: #fff;
        margin-top: .12rem;
        border-radius: .1rem;
        color: #ccc;
        line-height: .64rem;
        padding-left: .3rem;
    .header-right
      width: 1.24rem;
      flota: right;
      text-align: center;
</style>
