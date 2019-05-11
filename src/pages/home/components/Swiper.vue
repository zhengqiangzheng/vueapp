<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of imgList">

      <img :key="item.id" :src="item.url">

    </swiper-slide>

  </swiper>
    <div class="swiper-pagination"  slot="pagination"></div>
  </div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    data: function () {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop:true
        }
        ,imgList:[
          {id:1,url:'https://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/4c8629a965bb27e2216976f8302c0187.jpg'},
          {id:2,url:'https://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/8b75ece9943e703fc1b78f2d02a71bae.jpg'},
          {id:3,url:'https://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/973dc1ae0da73a58410186df08ff25cb.jpg'}
        ]

      }
    }}



</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background-color #eaeaea
  .wrapper
    overflow :hidden
    width :100%
    height :31.25vm
    .swiper-img
      width: 100%
  .swiper-pagination
    position :inherit





</style>
