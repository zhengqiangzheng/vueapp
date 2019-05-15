<template>
  <ul class="list">
 <li class="item">A</li>
 <li class="item">A</li>
 <li class="item">A</li>
 <li class="item">A</li>
 <li class="item">A</li>
 <li class="item">A</li>
 <li class="item">A</li>
  </ul>
</template>

<script>
  export default {
    name: 'CityAlphabet'
  }
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.style'
  .list
    display flex
    justify-content center
    position absolute
    top :1.58rem
    right 0
    bottom 0
    width  .99rem
    flex-direction column
    .item
      text-align center
      line-height .44rem
      margin-top .44rem
      color  $bgColor


</style>
