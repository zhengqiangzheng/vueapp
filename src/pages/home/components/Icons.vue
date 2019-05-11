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
    data(){
        return{
    swiperOption:{
      loop:true

    },
      iconList:  [
        {
          id:'1',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc:'热门景点'

        },{
          id:'2',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc:'一日游'
        },{
          id:'3',
          imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/3ef092d0a89ffddb7f781cda30c8ae49.png',
          desc:'上海上海'
        },{
          id:'4',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/f5/c4c9d9830404e602.png',
          desc:'室内娱乐'
        },{
          id:'5',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          desc:'辰山植物园'
        },{
          id:'6',
          imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/209908a8fc21779b485ab05f01835eaa.png',
          desc:'浦江郊野公园'
        },{
          id:'7',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/de/f26be47a6bf02a02.png',
          desc:'上海野生'
        },{
          id:'8',
          imgUrl:'https://img1.qunarzz.com/piao/fusion/1810/50/26ffa31b56646402.png',
          desc:'上海海昌'
        },{
          id:'9',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc:'上海海昌'
        }

          ]

        }
    },
    computed:{
      pages (){
        const pages = [];
        this.iconList.forEach((item,index)=>{
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
