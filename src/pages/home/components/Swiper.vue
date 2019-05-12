<template>
  <div class="wrapper">
    <!--这里的v-if是让swiper加载完成后创建-->
  <swiper :options="swiperOption" v-if="showSwiper">
    <swiper-slide v-for="item of list">

      <img :key="item.id" :src="item.imgUrl">

    </swiper-slide>

  </swiper>
    <div class="swiper-pagination"  slot="pagination"></div>
  </div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    props:{
      list :Array
    },
    data: function () {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop:true
        }

      }
    },
    computed:{
      showSwiper(){
        return this.list.length;
      }
    }
  }



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
