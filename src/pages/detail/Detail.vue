<template>
<div>
<detail-banner></detail-banner>
<detail-header></detail-header>
<div class="content">
  <detail-list :list="list"></detail-list>
</div>
</div>
</template>
<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'

export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '成人票',
        children: [{
          title: '成人票绅士手',
          children: [{
            title: '小孩子'
          }, {
            title: '小孩子'
          }]
        }, {
          title: '成人票五官'
        }]
      }, {
        title: '学生票'
      }, {
        title: '学2票'
      }, {
        title: '学23票'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .content
    height 50rem
</style>
