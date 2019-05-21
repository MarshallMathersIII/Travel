<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe6e1;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe6a8;输入城市/景点/游玩主题</span>
    </div>
  <router-link to="/city">
    <div class="header-right">{{this.doubleCity}}
      <span class="iconfont arrow-icon">&#xe688;</span>
    </div>
  </router-link>
  </div>
</template>
<script>
import { mapState, mapGetters } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city']),
    ...mapGetters(['doubleCity'])

  }
}
</script>
  <style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  @import '~styles/mixins.styl'
  .header
    display : flex
    line-height: $headerHeight
    background: $bgColor
    color : #ffffff
    .header-left
        width: .64rem
        float left
        .back-icon
          text-align : center
          font-size : .4rem
    .header-input
        margin-top : .13rem
        padding-left : .2rem
        flex : 1
        height : .64rem
        line-height : .64rem
        background : #ffffff
        border-radius : .1rem
        color : #ccc
    .header-right
        color white
        min-width: .1.04rem
        margin-left : .1rem
        margin-right : .1rem
        float right
        .arrow-icon
          font-size : .24rem
</style>
