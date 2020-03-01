<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/ed/bf2bc72af591d5.jpg_r_640x214_f9f1bfcc.jpg',
        title: '温泉必游',
        desc: '为你量身打造绿色健康生活方式，远离都市的喧嚣，工作的烦恼，还你一个悠闲静雅之旅'
      },
      {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/e1/cdbf56d837da59.jpg_r_640x214_105fc3f2.jpg',
        title: '民国情怀国共风华',
        desc: '南京，一座历史文化名城，这片土地上曾经经历过太多太多值得我们去追忆的往事'
      },
      {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/d3/7d775a7bb3f246.jpg_r_640x214_9c946be5.jpg',
        title: '汉文化景区',
        desc: '汉文化景区，北方故里，欢迎到来'
      },
      {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/58/a02ad3ab47e3e3.jpg_r_640x214_08977098.jpg',
        title: '徐州必游TOP10',
        desc: '徐州！你不可错过的风景'
      },
      {
        id: '0005',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/37/8a0cddbe99f5.jpg_r_640x214_fac8d255.jpg',
        title: '拓展·徐州',
        desc: '野战！约吗？'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top :.2rem
    line-height :.8rem
    background :#eee
    text-indent :.2rem
  .item-img-wrapper
    height :0
    overflow : hidden;
    padding-bottom :33.9%
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
