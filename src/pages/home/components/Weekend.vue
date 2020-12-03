<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
        <li class="weekend-item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="weekend-item-img" :src="item.imgUrl"/>
            </div>
            <div class="weekend-item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
            </div>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
   name: 'homeWeekend',
   data (){
       return {
        recommendList:[{
           id:'0001',
           imgUrl:"http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg",
           title:"大连海洋圣地",
           desc:"浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站"
       },{
           id:'0002',
           imgUrl:"http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg",
           title:"大连海洋圣地",
           desc:"浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站"
       },{
           id:'0003',
           imgUrl:"http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg",
           title:"大连海洋圣地",
           desc:"浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站浪漫大连首站"
       }]}
   }    
}
</script>

<style lang="stylus">
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .weekend-item-img
      width 100%
      padding 0 .1rem 0 .1rem
  .weekend-item-info
    width 1rem
    flex 1
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()

</style>