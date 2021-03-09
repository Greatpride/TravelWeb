<template>
    <ul class="list">
        <li class="item-word">a</li>
        <li class="item-word">a</li>
        <li class="item-word">a</li>
        <li class="item-word">a</li>
        <li class="item-word">a</li>
        <li class="item-word">a</li>
        <li class="item-word">a</li>
        <li class="item-word">a</li>
        <li class="item-word">a</li>
        <li class="item-word">a</li>
    </ul>
</template>

<script>
export default {
    name:'alphabet'
}
</script>

<style lang="stylus" rel='stylesheet/stylus' scoped>
  @import '~styles/varibles.styl'
  .list
    display flex 
    flex-direction column
    justify-content center
    position absolute
    top 1.58rem
    right 0
    bottom 0
    width .4rem
    .item-word
      line-height .4rem
      text-align  center
      color $bgColor
</style>