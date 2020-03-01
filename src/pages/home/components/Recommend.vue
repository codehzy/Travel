<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img :src= "item.imgUrl" alt="" class="item-img">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1505/3b/3b634562e4bc0d3c.water.jpg_200x200_df92fe33.jpg',
        tilte: '汉文化景区',
        desc: '汉文化景区，北方故里，欢迎到来'
      },
      {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1701/7b/7b76a9f05468aceaa3.water.jpg_200x200_f802496a.jpg',
        tilte: '潘安湖湿地公园',
        desc: '潘安湖湿地公园，丽水之都'
      },
      {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1505/3b/3b634562e4bc0d3c.water.jpg_200x200_df92fe33.jpg',
        tilte: '汉文化景区',
        desc: '汉文化景区，北方故里，欢迎到来'
      },
      {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1707/b7/b7b4bd266efd9e39a3.water.jpg_200x200_b044dcd2.jpg',
        tilte: '卧龙泉景区',
        desc: '卧龙泉景区，孔明是也'
      },
      {
        id: '0005',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1906/4b/4b1e81b4374afe3da3.img.jpg_200x200_d06f7241.jpg',
        tilte: '比如明天儿童体验乐园',
        desc: '比如明天儿童体验乐园,欢迎您您的孩子'
      },
      {
        id: '0006',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1701/7b/7b76a9f05468aceaa3.water.jpg_200x200_f802496a.jpg',
        tilte: '潘安湖湿地公园',
        desc: '潘安湖湿地公园，丽水之都'
      },
      {
        id: '0007',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1505/3b/3b634562e4bc0d3c.water.jpg_200x200_df92fe33.jpg',
        tilte: '汉文化景区',
        desc: '汉文化景区，北方故里，欢迎到来'
      },
      {
        id: '0008',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1707/b7/b7b4bd266efd9e39a3.water.jpg_200x200_b044dcd2.jpg',
        tilte: '卧龙泉景区',
        desc: '卧龙泉景区，孔明是也'
      },
      {
        id: '0009',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1906/4b/4b1e81b4374afe3da3.img.jpg_200x200_d06f7241.jpg',
        tilte: '比如明天儿童体验乐园',
        desc: '比如明天儿童体验乐园,欢迎您您的孩子'
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
  .item
    display :flex
    height :1.9rem
    .item-img
      width :1.7rem
      height :1.7rem
      padding :.1rem
    .item-info
        flex :1
        padding :.1rem
        min-width :0
      .item-title
        line-height :.54rem
        font-size :.32rem
        ellipse()
      .item-desc
        line-height: .4rem;
        color:#ccc
        ellipse()
      .item-button
        line-height :.44rem
        margin-top :.16rem
        padding :.2rem
        background :#ff9300
        color :#fff
        padding :0 .1rem
        border-radius :.06rem
</style>
