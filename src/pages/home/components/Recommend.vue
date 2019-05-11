<template>
  <div>
  <div class="recommend-title">
    热销推荐
  </div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList">
      <div class="item-img-wrapper">
        <img :src="item.imgUrl" class="item-img">
      </div>
      <div class="item-info">
        <p class="item-title">{{item.placeName}}</p>
        <p class="item-desc">{{item.describe}}</p>
        <button class="item-button">查看详情</button>
      </div>

    </li>

  </ul>
  </div>
</template>

<script>
  export default {
    name: 'HomeRecommend',
    data() {
      return{
        recommendList:[
          {id:'001',imgUrl:'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',placeName:'上海迪士尼乐园',describe:'全球最大的迪士尼城堡'},
          {id:'002',imgUrl:'http://img1.qunarzz.com/sight/p0/1904/d5/d579b03a110d75a8a3.img.jpg_200x200_740bd4c0.jpg',placeName:'上海野生动物园',describe:'会跳芭蕾的小海狮们~'},
          {id:'003',imgUrl:'http://img1.qunarzz.com/sight/p0/1811/e4/e4b9b471d2afc473a3.img.jpg_200x200_9a7794fc.jpg',placeName:'上海欢乐谷',describe:'敢上1200米长的木质过山车吗？'}

        ]


      }

    }
  }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.style"
  @import "~styles/mixins.style"
  .recommend-title
    margin-top .2rem
    background #eee
    text-indent .2rem
    font-size .80rem
    margin-top .9rem
    line-height 2.4rem
  .item
    display flex
    overflow hidden
    height 5.6rem
    .item-img
      width 100px
      height 100px
      padding  5px
    .item-info
      flex:1
      min-width 0
      padding:1.1rem
      .item-title
        line-height:.15px
        font-size:.98rem
      .item-desc
        line-height:15px
        color:#ccc
        ellipsis()
        padding-top 15px
      .item-button
        margin-top:10px
        background:#ff9300
        padding:0 .8rem
        border-radius:.06rem
        color:#fff






</style>
