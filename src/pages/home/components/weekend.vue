<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.list">
        <div class="item-img-wrapper">
          <img :src= "item.imgUrl" alt="" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    line-height :.8rem
    background :#eee
    text-indent :.2rem
  .item-img-wrapper
    height :0
    overflow : hidden;
    padding-bottom :37.09%
  .item-img
    width:100%
  .item-info
    padding :.1rem
    min-width :0
  .item-title
    line-height :.54rem
    font-size :.32rem
    ellipse()
  .item-desc
    line-height: .4rem;
    color:#616161
    font-size:.12rem
    ellipse()
</style>
