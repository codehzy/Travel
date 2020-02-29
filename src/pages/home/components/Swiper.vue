<template>
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="src-swiper" :src="item.imgUrl" alt="">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
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
      swiperList: [{
        id: '1001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/0b26e9760c2673c63c05e1efce1275ea.jpg_750x200_495c0a72.jpg'
      },
      {
        id: '1002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/0b26e9760c2673c63c05e1efce1275ea.jpg_750x200_495c0a72.jpg'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
      .src-swiper
              width :100%
</style>
