<template>
  <div>
    <div class="recommed-title">热销推荐</div>
    <ul>
      <router-link tag="li"
        class="item border-bottom"
        v-for="recommedItem in list"
        :key="recommedItem.id"
        :to="'/detail/' + recommedItem.id"
      >
        <img class="item-img" :src="recommedItem.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{recommedItem.title}}</p>
          <p class="item-desc">{{recommedItem.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
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
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
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
      .item-button
        background #ff9300
        padding 0 .1rem
        border-radius .06rem
        margin-top .16rem
        color #fff
        line-height .44rem
</style>
