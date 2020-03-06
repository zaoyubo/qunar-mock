<template>
  <div>
    <div class="recommed-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="recommedItem in list" :key="recommedItem.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="recommedItem.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{recommedItem.title}}</p>
          <p class="item-desc">{{recommedItem.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
    }
  },
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommed-title
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    height 0
    overflow hidden
    padding-bottom 33.9%
  .item-img
    width 100%
  .item-info
    flex 1
    padding .1rem
    min-width 0
    .item-title
      ellipsis()
      line-height .54rem
      font-size .32rem
    .item-desc
      ellipsis()
      line-height .4rem
      color #CCCCCC
</style>
