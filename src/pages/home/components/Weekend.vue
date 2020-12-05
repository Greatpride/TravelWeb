<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
        <li class="weekend-item border-bottom" v-for="item of list" :key="item.id">
            <div class="item-img-wrapper">
                <img class="weekend-item-img" :src="item.imgUrl"/>
            </div>
            <div class="weekend-item-info">
                <p class="item-title">{{item.name}}</p>
                <p class="item-desc">{{item.desc}}</p>
            </div>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
   name: 'homeWeekend',
   props:{
     list:Array
   }
}
</script>

<style lang="stylus">
  @import '~styles/mixins.styl'
  .title
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 37%
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