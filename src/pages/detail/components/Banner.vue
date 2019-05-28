<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg" >
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div class="banner-number"><span class="iconfont">&#xe63a;</span>{{this.bannerImgs.length}}</div>
      </div>
    </div>
    <common-gallary :imgs="bannerImgs" v-show="showGrallary" @close="handleGrallaryClose"></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    bannerImgs: Array
  },
  data () {
    return {
      showGrallary: false
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
