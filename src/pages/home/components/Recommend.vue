<template>
  <div>
    <div class="title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl" alt="">
      </div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </li>
  </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1703/ef/efca9bb3e360348aa3.water.jpg_200x200_5a7e26ce.jpg',
        title: '森晖自然博物馆',
        desc: '👍小伙伴们都收藏了，去看看吧~'
      },{
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/1d/1d756648039bf30f90.water.jpg_200x200_64da9a70.jpg',
        title: '亲子动物园',
        desc: '活水推助健康生活'
      },{
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1511/34/34170b200db08a5a90.img.jpg_200x200_cc3130fd.jpg',
        title: '银色假日水会',
        desc: '夏天玩水的天堂，适合全家一起玩'
      }]
    }
  }
}
</script>

<style scoped lang="scss">
  @import "~styles/variables";
  .title {
    margin-top: .2rem;
    line-height: .8rem;
    background: #eee;
    text-indent: .2rem;

  }
  .item {
    overflow: hidden;
    display: flex;
    height: 1.9rem;

    .item-img {
      width: 1.7rem;
      height: 1.7rem;
      padding: .1rem;
    }
    .item-info {
      flex:1;
      padding: .1rem;
      min-width: 0;
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
      .item-button {
        line-height: .44rem;
        margin-top: .16rem;
        background: #ff9300;
        padding: 0 .2rem;
        border-radius: .06rem;
        color: #fff;
      }
    }
  }

</style>
