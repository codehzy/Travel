<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="iconImg">
            <img  class="icon-img-content" :src="item.imgUrl" alt="">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'https://picbed.qunarzz.com/f5e5770393d759578962e53ee67798c8.png',
        desc: '景点门票'
      },
      {
        id: '0002',
        imgUrl: 'https://picbed.qunarzz.com/ae617a31e0bd5803d76918b817f6d942.png',
        desc: '自由行'
      },
      {
        id: '0003',
        imgUrl: 'https://picbed.qunarzz.com/377db8cb2143aebf01869c9baad3d325.png',
        desc: '汽车票船票'
      },
      {
        id: '0004',
        imgUrl: 'https://picbed.qunarzz.com/a36d2288f19e54562338f4d8ef986288.png',
        desc: '低价机票'
      },
      {
        id: '0005',
        imgUrl: 'https://picbed.qunarzz.com/f5e5770393d759578962e53ee67798c8.png',
        desc: '景点门票'
      },
      {
        id: '0006',
        imgUrl: 'https://picbed.qunarzz.com/ae617a31e0bd5803d76918b817f6d942.png',
        desc: '自由行'
      },
      {
        id: '0007',
        imgUrl: 'https://picbed.qunarzz.com/377db8cb2143aebf01869c9baad3d325.png',
        desc: '汽车票船票'
      },
      {
        id: '0008',
        imgUrl: 'https://picbed.qunarzz.com/a36d2288f19e54562338f4d8ef986288.png',
        desc: '低价机票'
      },
      {
        id: '0009',
        imgUrl: '//s.qunarzz.com/homenode/images/touchheader/flight.png',
        desc: '机票'
      },
      {
        id: '0010',
        imgUrl: 'https://picbed.qunarzz.com/377db8cb2143aebf01869c9baad3d325.png',
        desc: '汽车票船票'
      },
      {
        id: '0011',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '自然风光'
      },
      {
        id: '0012',
        imgUrl: '//s.qunarzz.com/homenode/images/touchheader/flight.png',
        desc: '机票'
      },
      {
        id: '0013',
        imgUrl: 'https://picbed.qunarzz.com/377db8cb2143aebf01869c9baad3d325.png',
        desc: '汽车票船票'
      },
      {
        id: '0014 ',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '自然风光'
      }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang ='stylus' scoped>
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"
  .icons >>> .swiper-container
    height :0
    padding-bottom :50%
  .icons
    margin-top :.2rem
    .icon
      position :relative
      float :left
      overflow :hidden
      width :25%
      height :0
      padding-bottom :25%
      .iconImg
        position :absolute
        top:0
        left:0
        right :0
        bottom : .30rem
        box-sizing : border-box
        padding:.1rem
        .icon-img-content
            display :block
            height  :100%
            margin : 0 auto
      .icon-desc
        position :absolute
        bottom:0
        left:0
        right :0
        text-align :center
        height : .44rem
        line-height :.44rem
        color :$darkTextColor
        ellipse()
</style>
