<template>
  <div class="list">
    <div class="area">
      <div class="title border-topbottom" id="nowcity">当前城市</div>
      <div class="button-list">
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
    </div>
      <div class="area">
        <div class="title border-topbottom" id="dqcs">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>

      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom" border-bottom>阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom" border-bottom>阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom" border-bottom>阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom" border-bottom>阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
        </div>
      </div>
  </div>
  </div>
</template>

<script>
  export default {
    name: 'CityList'
  }
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.style'
  .border-topbottom
    &:before
      border-color:#ccc
    &:after
      border-color:#ccc
  .list
    position absolute
    margin-top 40px
    overflow hidden
    top 0
    left 0
    right 0
    bottom 0
    top :0
    #nowcity
     margin-top 15px
    #dqcs
      margin-top 15px
    .title
      margin-top 0px
      Line-height: 13px
      background:#eee
      padding-left:.2rem
      color:#666
      font-size:.26rem
    .button-list
      overflow hidden
      padding:.1rem .6rem .1rem .1rem
    .button-wrapper
      float: left
      width 33.33%
    .button
      margin .5rem
      border .02rem solid #ccc
      text-align center
      font-size 5px
      border-radius .6rem
    .item-list
      .item
        line-height .76rem
        color #666
        padding-left .2rem
        padding-bottom 10px
        margin-top 10px
        font-size 12px


  </style>
