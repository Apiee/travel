<template>
  <div>
    <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl" alt="">
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
  name: 'HomeRecommend',
  props: {
    weekendList: Array
  },
  data () {
    return {
      /* weekendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg',
        title: '森晖自然博物馆',
        desc: '👍小伙伴们都收藏了，去看看吧~'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
        title: '亲子动物园',
        desc: '活水推助健康生活'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f8/29dfa785277839.jpg_r_640x214_7d051523.jpg',
        title: '银色假日水会',
        desc: '夏天玩水的天堂，适合全家一起玩'
      }] */
    }
  }
}
</script>

<style scoped lang="scss">
  @import "~styles/variables";
  .title {
    line-height: .8rem;
    background: #eee;
    text-indent: .2rem;

  }
  .item {
    .item-img-wrapper {
      overflow: hidden;
      height: 0;
      padding-bottom: 37.09%;
    }
    .item-img {
      width: 100%;
    }
    .item-info {
      padding: .1rem;
      .item-title {
        line-height: .54rem;
        font-size: .32rem;
        @include ellipsis;
      }
      .item-desc {
        line-height: .4rem;
        color: #ccc;
        @include ellipsis;
      }
    }
  }

</style>
