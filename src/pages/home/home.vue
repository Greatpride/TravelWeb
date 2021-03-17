<template>
    <div>
        <home-header></home-header>
        <home-swiper :list = "swiperList"></home-swiper>
        <home-icons :icons="iconList"></home-icons>
        <home-recommend :list = "recommendList"></home-recommend>
        <home-weekend :list = "weekendList"></home-weekend>
    </div>
</template>

<script>
import homeHeader from './components/Header';
import homeSwiper from './components/Swiper';
import homeIcons from './components/Icons';
import homeRecommend from './components/Recommend';
import homeWeekend from './components/Weekend';
import axios from 'axios';

export default {
    name:'home',
    components:{
        homeHeader: homeHeader,
        homeSwiper: homeSwiper,
        homeIcons:homeIcons,
        homeRecommend:homeRecommend,
        homeWeekend:homeWeekend
    },
    data () {
      return {
          swiperList: [],
          iconList:[],
          recommendList:[],
          weekendList:[]
      }
    },
    methods : {
        getHomeInfo (){
            axios.get('/api/index.json')
              .then(this.getHomeInfoSucc)
        },
        getHomeInfoSucc(res){
            res = res.data;
            if (res.ret&&res.data){
                const data = res.data
                console.log(data)
                this.swiperList = data.bannerList
                this.iconList = data.iconList
                this.recommendList = data.recommendList
                this.weekendList = data.weekendList
            }
        }
    },
    mounted () {
        this.getHomeInfo()
    }
}
</script>

<style>
</style>