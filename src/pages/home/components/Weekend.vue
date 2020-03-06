<template>
  <div>
    <div class="recommed-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="recommedItem in recommedList" :key="recommedItem.id">
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
      recommedList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        title: '北京赏花好地方',
        desc: '乱花渐欲迷人眼，京城赏花大搜索'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        title: '北京赏花好地方',
        desc: '乱花渐欲迷人眼，京城赏花大搜索'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        title: '北京赏花好地方',
        desc: '乱花渐欲迷人眼，京城赏花大搜索'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        title: '北京赏花好地方',
        desc: '乱花渐欲迷人眼，京城赏花大搜索'
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
