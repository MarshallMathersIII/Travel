<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe6e1;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe6a8;输入城市/景点/游玩主题</span>
    </div>
    <div class="header-right">
      <span class="iconfont arrow-icon">城市&#xe688;</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>
  <style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  .header
    display : flex
    line-height: .86rem
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
        width: .1.24rem
        margin-left : .1rem
        margin-right : .1rem
        float right
        .arrow-icon
          font-size : .24rem
</style>
