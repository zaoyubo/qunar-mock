<template>
  <div class="banner">
    <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_600x330_b40971b4.jpg"/>
    <div class="banner-info">
      <div class="banner-title">八达岭长城(AAAAA景区)</div>
      <div class="banner-number">
        <span class="iconfont banner-icon"> &#xe692; </span>
        39
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailBanner'
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0,0,0,0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        padding 0 .32rem
        margin-top .14rem
        height .4rem
        font-size .24rem
        line-height .4rem
        border-radius .4rem
        background rgba(0,0,0,0 .8)
        .banner-icon
          font-size .24rem

</style>
