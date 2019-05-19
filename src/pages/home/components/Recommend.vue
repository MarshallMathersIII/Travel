<template>
<div>
<div class="title">热销推荐</div>
  <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" v-bind:src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
        </div>
      </li>
  </ul>
</div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return ({
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/p/tts4/1805/50/f698d653d5b4fe02.jpg_110x110_06c3a39a.jpg',
        title: '上海1日游',
        desc: '上海博物馆+东方明珠+浦江游游+上海博物馆+东方明珠+浦江游游'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/p/tts4/1805/50/f698d653d5b4fe02.jpg_110x110_06c3a39a.jpg',
        title: '上海2日游',
        desc: '上海博物馆+东方明珠+浦江游游+上海博物馆+东方明珠+浦江游游'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/p/tts4/1805/50/f698d653d5b4fe02.jpg_110x110_06c3a39a.jpg',
        title: '上海3日游',
        desc: '上海博物馆+东方明珠+浦江游游+上海博物馆+东方明珠+浦江游游'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/p/tts4/1805/50/f698d653d5b4fe02.jpg_110x110_06c3a39a.jpg',
        title: '上海4日游',
        desc: '上海博物馆+东方明珠+浦江游游+上海博物馆+东方明珠+浦江游游'
      }]
    })
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  line-height .8rem
  background #eeeeee
  margin-top .2rem
  text-indent .2rem
.item
  display flex
  height 1.9rem
  overflow hidden
  .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
  .item-info
    display flex 1
    padding  .1rem
    min-width 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
        line-height .4rem
        color #cccccc
        ellipsis()
    .item-btn
      line-height .44rem
      margin-top .16rem
      background #ff9300
      padding 0 .2rem
      border-radius .06rem
      color #ffffff
</style>
