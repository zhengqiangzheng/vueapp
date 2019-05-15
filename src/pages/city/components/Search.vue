<template>
  <div>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音" />
  </div>
  </div>
</template>

<script>
  export default {
    name: 'CityHeader'
  }
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.style'
  .search
    height: 10px
    padding: 0 .1rem
    background: $bgColor
    .search-input
      width: 100%
      height: 1rem
      padding .4rem .5rem
      margin-top 6px
      margin-bottom 10px
      line-height: 10px
      text-align: center
      border-radius: .06rem
      color: #666

</style>
