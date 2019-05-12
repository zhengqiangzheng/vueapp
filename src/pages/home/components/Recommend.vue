<template>
  <div>
  <div class="recommend-title">
    热销推荐
  </div>
  <ul>
    <li class="item border-bottom" v-for="item of list">
      <div class="item-img-wrapper">
        <img :src="item.imgUrl" class="item-img">
      </div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>

    </li>

  </ul>
  </div>
</template>

<script>
  export default {
    name: 'HomeRecommend',
    props:{
      list :Array
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
      width 178px
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
