<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper" v-for="hotcity in hotCities" :key="hotcity.id">
            <div class="button">{{hotcity.name}}</div>
          </div>
        </div>
      </div>

      <div class="area" v-for="(val,key,index) in  cities" :key="index">
        <div class="title border-topbottom">{{key}}</div>
        <div class="item-list" >
          <div class="item border-bottom" v-for="item in val" :key="item.id">{{item.name}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'List',
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  },
  props: {
    hotCities: Array,
    cities: Object
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
  .border-bottom
    &:before
      border-color: #ccc
  .list
    position absolute
    top 1.58rem
    right 0
    left 0
    bottom 0
    overflow hidden
    .title
      line-height .54rem
      background #eee
      padding-left .2rem
      color #666
      font-size .26rem
    .button-list
      padding .1rem .6rem .1rem .1rem
      overflow hidden
      .button-wrapper
        float left
        width 33.33%
        .button
          padding .1rem 0
          text-align center
          margin .1rem
          border .02rem solid #ccc
          border-radius .06rem
    .item-list
      .item
        line-height .76rem
        padding-left .2rem
</style>
