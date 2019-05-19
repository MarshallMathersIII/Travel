<template>
  <div class="icons">
    <swiper>
    <swiper-slide v-for="(page,index) of pages" :key="index">
      <div class="icon" v-for="item of page" :key="item.id">
        <div class="icon-img">
          <img class="icon-img-content" :src='item.imgUrl'/>
        </div>
        <p class="icon_desc">{{item.desc}}</p>
      </div>
    </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data: function () {
    return ({
      iconList: [{
        id: '0001',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '一日游啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊'
      }, {
        id: '0002',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '2日游'
      }, {
        id: '0003',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '3日游'
      }, {
        id: '0004',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '4日游'
      }, {
        id: '0005',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '一日游'
      }, {
        id: '0006',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '一日游'
      }, {
        id: '0007',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '一日游'
      }, {
        id: '0008',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '一日游'
      }, {
        id: '0009',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '9日游'
      }, {
        id: '0010',
        imgUrl: 'https://dimg02.c-ctrip.com/images/100t0l000000d61ht687A.png',
        desc: '10日游'
      }]

    })
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
    margin-top .1rem
  .icon
    overflow hidden
    position  relative
    width: 25%
    height 0
    float left
    padding-bottom: 25%
    .icon-img
      text-align:center
      position  absolute
      top 0
      left 0
      right 0
      bottom  .44rem
      box-sizing : border-box
      padding .1rem
      .icon-img-content
        display inline-block
        height 100%
    .icon_desc
      position  absolute
      left 0
      right 0
      bottom  0
      height .44rem
      line-height .44rem
      text-align center
      color $darkTextColor
      ellipsis()

</style>
