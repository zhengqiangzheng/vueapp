<template>
  <div class="header">
    <div class="header-left" ><div class="iconfont back-icon">&#xe624;</div></div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont arrow-icon">&#xe605;</span>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HomeHeader',
    props:{
      city :String
    }
  }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.style"
  .header
    display: flex
    line-height: .86rem
    background-color: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      margin-right :.35rem

      .back-icon
        text-align :center
        font-size :.4rem
        margin-top :.20rem
        padding-left :.2rem



    .header-input
      flex: 1
      height :.99rem
      line-height: .99 rem
      margin-top: .20rem
      margin-bottom :.10rem
      font-size :.4rem
      margin-left: .2rem
      padding-left: .2rem
      border-radius: .1rem
      background: #fff
      color: #ccc
    .header-right
      min-width: 1.04rem
      margin-top :.2rem
      padding: 0 .1rem
      float: right
      text-align: center
      color: #fff
      font-size :.4rem
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem



</style>
