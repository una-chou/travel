<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.key">
        <img class="swiper-img" :src="item.imgUrl" alt="">
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
      swiperList: [{
        id: '001',
        imgUrl: 'https://img1.qunarzz.com/p/tts2/1807/db/209f570928b7eb02.jpg_r_640x420x90_6793c7b5.jpg'
      }, {
        id: '002',
        imgUrl: 'https://img1.qunarzz.com/p/tts7/1804/79/3f3c36690c550302.jpg_r_640x420x90_6b5e4d52.jpg'
      }, {
        id: '003',
        imgUrl: 'https://img1.qunarzz.com/p/tts5/1806/9e/316f34c7bf48eb02.jpg_r_640x420x90_bfa80020.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 66.67%
  .swiper-img
    width: 100%
</style>
