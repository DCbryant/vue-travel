<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img
          class="swiper-img"
          :src="item.imgUrl"
        />
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
      swiperList: [
        {
          id: '11',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/b5/8bd6da9d794e1902.jpg_750x200_b1a28179.jpg'
        },
        {
          id: '22',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/dd/466fb314a22bd702.jpg_750x200_25ea4968.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  // 样式穿透，不受scope控制
  .wrapper >>> .swiper-pagination-bullet-active
      background: #fff !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    // 图片宽高比始终占据26.67%
    // 或者：width: 26.67vw
    padding-bottom: 26.67%
    background: #eee
    .swiper-img
      width: 100%
</style>
