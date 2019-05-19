<template>
  <div class="header">城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe6e1;</div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'CityHEader'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';

.header
  overflow: hidden
  height: $headerHeight
  line-height: $headerHeight
  text-align: center
  color: #ffffff
  background: $bgColor
  position relative
  font-size: 0.32rem
  .header-back
    position absolute
    top 0
    left 0
    width .64rem
    text-align center
    font-size .4rem
    color #eeeeee
</style>
