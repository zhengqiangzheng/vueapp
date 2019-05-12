<template>
  <div>
    <home-Header :city="city"></home-Header>
    <home-Swiper :list="swiperList"></home-Swiper>
    <home-icons :list="iconList"></home-icons>
    <home-recommend :list="recommendList"></home-recommend>
    <home-weekend :list="weekendList"></home-weekend>
  </div>
</template>

<script>
  import HomeHeader from './components/Header'
  import HomeSwiper from './components/Swiper'
  import HomeIcons from './components/Icons'
  import HomeRecommend from './components/Recommend'
  import HomeWeekend from './components/Weekend'
  import axios from 'axios'

  export default {
    name: 'Home',
    components: {
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeRecommend,
      HomeWeekend
    },
    methods:{
     getHomeInfo:function () {
       axios.get('api/index.json')
         .then(this.getHomeInfoSuccess)
     },
      getHomeInfoSuccess:function (res) {
       res=res.data
        if (res.ret && res.data) {
          const data = res.data;
          this.city=data.city
          this.swiperList = data.swiperList;
          this.iconList=data.iconList
          this.recommendList=data.recommendList
          this.weekendList=data.weekendList
        }
        console.log(res);

      }
    },
    mounted() {
      this.getHomeInfo();

    },
    data(){
      return {
        city :'',
        swiperList:[],
        iconList:[],
        recommendList:[],
        weekendList:[]
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
