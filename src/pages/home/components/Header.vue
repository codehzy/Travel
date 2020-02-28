<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-input">
      <span  class="iconfont" back-icon>&#xe632;</span>
      输入城市/经典/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}

</script>

<style lang="stylus" scoped>
  @import '~styles/iconfont/varibles.styl'
  .header
    display:flex
    line-height :.86rem
    background:$bgColor
    color:#fff
  .header-left
      width : .64rem
      float :left
      margin-left:.1rem
      .back-icon
          text-align :center
          font-size :.4rem
  .header-input
      flex : 1
      height :.64rem
      line-height :.64rem
      margin-top:.12rem
      padding-left:.2rem
      background:#fff
      border-radius :.10rem
      color : #ccc
  .header-right
      width :1.24rem
      text-align :center
      float :right
      .arrow-icon
        font-size:.24rem

</style>
