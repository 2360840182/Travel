<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/ed/bf2bc72af591d5.jpg_r_640x214_f9f1bfcc.jpg',
        title: '温泉必游',
        desc: '为你量身打造绿色健康生活方式，远离都市的喧嚣，工作的烦恼，还你一个悠闲静雅之旅'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/f1/ae9d4299b8aaea.jpg_r_640x214_0c555905.jpg',
        title: '南京必打卡',
        desc: '看尽王侯将相荣辱成败，六朝金粉潮起潮落'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1507/ae/bf7adc6c9b80fe.jpg_r_640x214_8e68e99f.jpg',
        title: '细数南京温泉',
        desc: '融人文景观与自然风光为一体的温泉圣地，温泉疗养、度假休闲的好去处'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
    padding: .2rem
    .item-title
      line-height: .54rem
      font-size: .32rem
    .item-desc
      color: #000
      line-height: .4rem
      ellipsis()
</style>
