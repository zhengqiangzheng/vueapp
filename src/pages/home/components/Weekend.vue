<template>
  <div>
  <div class="weekend-title">
    周末去哪儿
  </div>
  <ul>
    <li class="item border-bottom" v-for="item of list">
      <div class="item-img-wrapper">
        <img :src="item.imgUrl" class="item-img">
      </div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
      </div>

    </li>

  </ul>
  </div>
</template>

<script>
  export default {
    name: 'HomeWeekend',
    props:{
      list :Array
    }
  }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.style"
  @import "~styles/mixins.style"
  .weekend-title
    background #eee
    text-indent .2rem
    font-size .80rem
    line-height 2.4rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 37.09%
  .item-img
    width 100%
    padding-top 10px
  .item-info
    padding:.1rem
    .item-title
      line-height:10px
      font-size:.88rem
    .item-desc
      line-height:15px
      color:#ccc
      ellipsis()
      padding-top 15px

</style>
