<template>
  <div>
  <div class="weekend-title">
    周末去哪儿
  </div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList">
      <div class="item-img-wrapper">
        <img :src="item.imgUrl" class="item-img">
      </div>
      <div class="item-info">
        <p class="item-title">{{item.placeName}}</p>
        <p class="item-desc">{{item.describe}}</p>
      </div>

    </li>

  </ul>
  </div>
</template>

<script>
  export default {
    name: 'HomeWeekend',
    data() {
      return{
        recommendList:[
          {id:'001',imgUrl:'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',placeName:'上海必打卡',describe:'中西合璧，现代和传统各有各的精彩'},
          {id:'002',imgUrl:'http://img1.qunarzz.com/sight/source/1603/ad/69b0fc5f48ad5f.jpg_r_640x214_b0fd5c7b.jpg',placeName:'周末亲子爱玩',describe:'走进自然或玩转乐园，感知大千世界，游乐项目惊险刺激，特色表演异彩纷呈，等你们~~'},
          {id:'003',imgUrl:'http://img1.qunarzz.com/sight/source/1511/1d/fe098e8cfec117.jpg_r_640x214_a9be292a.jpg',placeName:'上海城市观光',describe:'来这里寻找你所不认识的魔都 ，感受云端漫步，品味老上海风情，享受休闲时光？'}

        ]


      }

    }
  }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.style"
  @import "~styles/mixins.style"
  .weekend-title
    margin-top .2rem
    background #eee
    text-indent .2rem
    font-size .80rem
    margin-top .9rem
    line-height 2.4rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
  .item-img
    width 100%
    padding-top 10px
  .item-info
    padding:1.1rem
    .item-title
      line-height:10px
      font-size:.88rem
    .item-desc
      margin-top .1rem
      line-height:15px
      color:#ccc
      ellipsis()
      padding-top 15px

</style>
