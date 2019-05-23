<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1811/e4/e4b9b471d2afc473a3.img.jpg_600x330_df3d1e0a.jpg" >
      <div class="banner-info">
        <div class="banner-title">上海欢乐谷(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont">&#xe63a;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGrallary" @close="handleGrallaryClose"></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGrallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1811/d5/d5153b5e337c0644a3.water.jpg_r_800x800_5785f05e.jpg', 'http://img1.qunarzz.com/sight/p0/1811/d5/d5153b5e337c0644a3.water.jpg_r_800x800_5785f05e.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGrallary = true
    },
    handleGrallaryClose () {
      this.showGrallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl';
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
      bottom  0
      line-height .6rem
      color #ffffff
      background-image linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
    .banner-title
      flex 1
    .banner-number
      margin-top .14rem
      padding 0 .4rem
      height .4rem
      line-height .4rem
      border-radius .2rem
      background rgba(0,0,0,.8)
</style>
