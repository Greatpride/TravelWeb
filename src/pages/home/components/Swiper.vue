<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
       <swiper-slide v-for="item of swiperList" :key="item.id">
           <img class="swiper-img" :src="item.imgUrl" />
       </swiper-slide>
       <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
    name:'homeSwiper',
    data(){
        return{
            swiperOption: {
                pagination:'.swiper-pagination',
                loop:true
            },
            swiperList: [{
                id:'001',
                imgUrl:'http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg'
            },{
                id:'002',
                imgUrl:'http://img1.qunarzz.com/sight/source/1812/fe/208e0360d686b8.jpg_r_640x214_7b9e6607.jpg'
            }]
        }
    }
}
</script>

<style lang="stylus" scope>
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    background #eee

    .swiper-img
      width 100%
    

</style>