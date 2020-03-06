<template>
  <div>
    <div class="recommed-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="recommedItem in recommedList" :key="recommedItem.id">
        <img class="item-img" :src="recommedItem.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{recommedItem.title}}</p>
          <p class="item-desc">{{recommedItem.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommedList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/ce/ce94534274b3bd6db4.water.jpg_200x200_91a2f180.jpg',
        title: '清华大学',
        desc: '北京市海淀区,北京高等学府'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/ce/ce94534274b3bd6db4.water.jpg_200x200_91a2f180.jpg',
        title: '清华大学',
        desc: '北京市海淀区,北京高等学府'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/ce/ce94534274b3bd6db4.water.jpg_200x200_91a2f180.jpg',
        title: '清华大学',
        desc: '北京市海淀区,北京高等学府'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/ce/ce94534274b3bd6db4.water.jpg_200x200_91a2f180.jpg',
        title: '清华大学',
        desc: '北京市海淀区,北京高等学府'
      }]
    }
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
