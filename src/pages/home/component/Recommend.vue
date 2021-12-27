<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img :src="item.imgUrl" class="item-img">
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
  data() {
    return {
      recommendList: [
        {
          id: 1,
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
          title: '故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿',
          desc: '浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿',
        },
        {
          id: 2,
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
          title: '故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿',
          desc: '浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿',
        },
        {
          id: 3,
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
          title: '故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿',
          desc: '浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿',
        },
        {
          id: 4,
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
          title: '故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿',
          desc: '浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿',
        },
        {
          id: 5,
          imgUrl: 'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
          title: '故宫博物院故宫博物院故宫博物院浪漫北京首站，帝王宫殿',
          desc: '浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿浪漫北京首站，帝王宫殿',
        },
      ]

    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title {
    margin-top: .2rem;
    line-height: .8rem;
    background: #eee;
    text-indent: .2rem;
  }
  ul {
    margin: 0;
    padding: 0;
  }
  p {
    margin: 0;
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
      flex: 1;
      padding: .1rem;
      min-width: 0;
      .item-title {
        line-height: .54rem;
        font-size: .32rem;
        ellipsis();
      }
      .item-desc {
        line-height: .4rem;
        color: #ccc;
        ellipsis();
      }
      .item-button {
        line-height: .44rem;
        margin-top: .16rem;
        background: #ff9300;
        padding: 0 .2rem;
        border: 0;
        border-radius: .06rem;
        color: #fff;
      }
    }
  }
</style>