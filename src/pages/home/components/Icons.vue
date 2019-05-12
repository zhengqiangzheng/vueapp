<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
    <div class="icon" v-for="item of page">
      <div class="icon-img">
      <img :src="item.imgUrl" :key="item.id" class="icon-img-content">
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
    props:{
      list :Array

    },
    data() {
      return {
        swiperOption: {
          autoplay:false
        }
      }
    },
    computed:{
      pages (){
        const pages = [];
        this.list.forEach((item,index)=>{
          const page = Math.floor(index / 8);
          if (!pages[page]) {
            pages[page]=[]
          }
          pages[page].push(item);
        })
        return pages;
      }
    }
  }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.style"
  @import "~styles/mixins.style"

  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icon
    position :relative
    overflow :hidden
    height :0
    float: left
    width :25%
    padding-bottom :25%
    .icon-img
      position absolute
      top :0
      left :0
      right :0
      bottom :.44rem
      box-sizing border-box
      height 1.1rem
      padding .1rem
      .icon-img-content
        height :3.8rem
        display block
        margin 0 auto
    .icon-desc
      font-size .80rem
      position absolute
      text-align center
      left :0
      right :0
      height .70rem
      line-height .44rem
      padding-top .44rem
      color $darkTextColor
      ellipsis()
      bottom :0






</style>
